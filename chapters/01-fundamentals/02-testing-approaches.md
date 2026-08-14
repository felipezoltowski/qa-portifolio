# Testing Approaches
## 1. Black-Box 
Black-box testing revolves around testing the software behaviour purely based on end-user perspective. You don't have access to softwares internal implementation.

The teste focuses on:
- Inputs
- User actions
- Business Rules
- Expected outputs
- Error handling

### Working Example

**Scenario:** Search for an accountant client.

The user enters a client name in the search field and expects the application to display matching results.

#### Test Case

| Step | Action | Expected Result |
|---|---|---|
| 1 | Open Accountant Connect | Dashboard is displayed |
| 2 | Navigate to the client list | Client list is displayed |
| 3 | Enter `John` in the search field | Search is executed |
| 4 | Review the results | Clients matching `John` are displayed |
| 5 | Clear the search | Full client list is displayed |

### Cypress Example

```Javascript
describe('Client Search', () => {
  it('should display clients matching the search term', () => {
    cy.visit('/clients');

    cy.get('[data-testid="client-search"]')
      .type('John');

    cy.contains('John').should('be.visible');
  });
});
```

## 2. White-Box
White-box testing revolves around testing the software internal implementation by validating logic, loops and statement coverage, functions, conditions, branchs and data-processing logic.

### Working Example

**Scenario:** Client filtering. Suppose we havea function responsible for filtering the client list.

```Javascript
function filterClients(clients, searchTerm) {
  if (!searchTerm) {
    return clients;
  }

  return clients.filter(client =>
    client.name.toLowerCase().includes(searchTerm.toLowerCase())
  );
}
```
### Mocha Example for Node.js Unit Testing
```Javascript
describe('filterClients', () => {
  const clients = [
    { name: 'John Smith' },
    { name: 'Jane Doe' },
    { name: 'Johnny Wilson' }
  ];

  it('should return matching clients', () => {
    const result = filterClients(clients, 'John');

    expect(result).to.deep.equal([
      { name: 'John Smith' },
      { name: 'Johnny Wilson' }
    ]);
  });

  it('should return all clients when search term is empty', () => {
    const result = filterClients(clients, '');

    expect(result).to.deep.equal(clients);
  });

  it('should return an empty array when there are no matches', () => {
    const result = filterClients(clients, 'Robert');

    expect(result).to.deep.equal([]);
  });
});
```

## 3. "Grey-Box"
While not being recognized as an standard per CTFL certification, its defined as a method that mixes black and white box testing, by giving slight knowledge of the software internals.