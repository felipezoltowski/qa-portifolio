# Test Oracle — Cart Feature (saucedemo.com)

## What Is a Test Oracle?
A test oracle is the mechanism used to determine whether an actual result is correct — it answers *"how do I know this is right?"* separately from the test steps themselves.

## Feature Under Test
Cart badge count behavior: the number displayed on the cart icon should always reflect the actual number of items currently in the cart.

**Test case:** Add one item to the cart, then remove it. Verify the cart badge updates correctly at each step (0 → 1 → 0).

### Oracle Sources

| Source | Oracle Statement | Justification |
|---|---|---|
| **1. Spec** | No formal specification is published for saucedemo. In its absence, the inferred requirement is: *cart badge count = number of items currently in cart*. | This is the most basic, implicit contract any cart UI should satisfy, even without a written doc. |
| **2. Comparable product** | On Amazon and similar e-commerce sites, the cart badge updates immediately after an add/remove action, without requiring a page refresh. | Real-world products serve as a reference for "expected" behavior when no spec exists. This oracle is weaker than a spec — it reflects convention, not a contractual requirement for saucedemo specifically. |
| **3. User expectation** | A user expects the badge to update instantly and accurately after any cart action, since a stale or incorrect count would misrepresent the cart's actual state and erode trust in the UI. | Grounded in general usability principles (state consistency, immediate feedback), not documentation. |

### Oracle Conflict / Resolution
If saucedemo's badge behavior diverges from the comparable-product oracle (e.g., delayed update, or no decrement on removal), the **user-expectation oracle takes priority** for judging pass/fail, since the core purpose of the badge is accurate, real-time state — not matching another product's specific implementation. The comparable-product oracle is treated as supporting evidence, not the final authority.

### Summary
In the absence of a formal spec, testers must combine multiple oracle sources and explicitly state which one governs the pass/fail decision. Here, user expectation (accurate, immediate feedback) is the deciding oracle, with comparable-product behavior used to justify what "accurate and immediate" should look like.


## Feature Under Test
Cart item displayed value behavior: the value of each product showed in the card must reflect the actual value on the dashboard display.

**Test case:** Add one item to the cart and verify if the shows acording to the value shown in the dashboard,

## Oracle Sources

| Source | Oracle Statement | Justification |
|---|---|---|
| **1. Spec** | No formal specification is published for saucedemo. In its absence, the inferred requirement is: *item dashboard value = cart item value*. | This is the most basic, implicit contract any cart UI should satisfy, even without a written doc. |
| **2. Comparable product** | On Amazon and similar e-commerce sites, the item value showed in dashboards equals that showed in cart, without requiring a page refresh. | Real-world products serve as a reference for "expected" behavior when no spec exists. This oracle is weaker than a spec — it reflects convention, not a contractual requirement for saucedemo specifically. |
| **3. User expectation** | A user expects value to be equal to those shown in the main dashboard, since a stale or incorrect count would misrepresent the cart's actual state and erode trust in the UI. | Grounded in general usability principles (state consistency, immediate feedback), not documentation. |

## Oracle Conflict / Resolution
If the cart price were to diverge from the dashboard price (e.g., due to tax being added only in the cart, rounding differences, or a stale cached value), the **spec/internal-consistency oracle takes priority** for judging pass/fail, since price accuracy is a direct, self-contained fact within the app — not dependent on matching another product's implementation. The comparable-product and user-expectation oracles serve as supporting justification for *why* this consistency matters, not as tie-breakers.

## Summary
Unlike oracles based on convention or inferred UX intent, this is an **internal consistency oracle**: the cart price is checked directly against the dashboard price within the same application, requiring no external reference. This makes it one of the most objective and easily verifiable oracle types, though the resolution note above still applies if a legitimate reason for divergence (e.g., tax) exists.