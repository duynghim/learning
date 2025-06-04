## Transaction
- A collection of queries
- One unit of work
- E.g Account deposit (select, update, update)

## Transaction Lifespan
- Transaction BEGIN
- Transaction COMMIT
- Transaction Rollback
- Transaction unexpected ending = Rollback (for example, crash)

## Nature of Transaction
- Transactions typically play a key role in updating and modifying data.
- However, it is normal to have a read-only transaction
- For Example, you want to generate a report, and you want to get consistent snapshot based at the time of transactions
