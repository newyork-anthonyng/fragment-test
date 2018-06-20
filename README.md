# Document Fragments

This code example shows the performance of using [`createDocumentFragment`](https://developer.mozilla.org/en/docs/Web/API/Document/createDocumentFragment) to add DOM Nodes.

# JS Perf Tests

We ran two tests with two test cases each (four scenarios) total.
[In the first two tests](https://jsperf.com/newyork-anthonyng-document-fragment-performance/1), we append 100,000 DOM nodes to our page. For one test, we used `document fragments`; for the other, we did not.
[In the last two tests](https://jsperf.com/newyork-anthonyng-document-fragment-performance-2), we append 1,000 DOM nodes to our page. For one test, we used `document fragments`; for the other, we did not.

| Scenario                          | Result (larger numbers are member)              |
| --------------------------------- | ----------------------------------------------- |
| Without Fragments (100,000 nodes) | 69.59% faster (compared to `with fragments`)    |
| With Fragments (100,000 nodes)    | 43.79% slower (compared to `without fragments`) |
| Without Fragments (1,000 nodes)   | 132 ops/sec                                     |
| With Fragments (1,000 nodes)      | 62.53 ops/sec                                   |