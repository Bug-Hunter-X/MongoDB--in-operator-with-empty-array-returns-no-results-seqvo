# MongoDB $in operator with empty array
This example demonstrates a common error when using the `$in` operator with an empty array in MongoDB queries.  The query `db.collection.find({ field: { $in: [] } })` will always return an empty array, even if the 'field' is null or undefined in some documents. This can be unexpected behavior.

The solution shows how to handle this by using alternative queries or explicitly checking for null or undefined values before applying the `$in` operator.