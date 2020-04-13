digraph {
    graph [pad="0.5", nodesep="0.5", ranksep="1"];
    node [shape=plain]
    rankdir=LR;

Submissions [label=<
<table border="0" cellborder="1" cellspacing="0">
  <tr><td><b>Submissions</b></td></tr>
  <tr><td port="1">User ID</td></tr>
  <tr><td port="2">Submission ID</td></tr>
  <tr><td port="3">Input Type</td></tr>
  <tr><td port="4">Measurements</td></tr>
</table>>];

UserHistory [label=<
<table border="0" cellborder="1" cellspacing="0">
  <tr><td><b>UserHistory</b></td></tr>
  <tr><td port="1">Result ID</td></tr>
  <tr><td port="2">User ID</td></tr>
  <tr><td port="3">Result Log</td></tr>
</table>>];

Users [label=<
<table border="0" cellborder="1" cellspacing="0">
  <tr><td><b>Users</b></td></tr>
  <tr><td port="1">User ID</td></tr>
  <tr><td port="2">First Name</td></tr>
  <tr><td port="3">Last Name</td></tr>
  <tr><td port="4">Email</td></tr>
  <tr><td port="5">Username</td></tr>
  <tr><td port="6">Password</td></tr>
</table>>];

Calculations [label=<
<table border="0" cellborder="1" cellspacing="0">
  <tr><td><b>Calculations</b></td></tr>
  <tr><td port="1">Calculation ID</td></tr>
  <tr><td port="2">Calculation Method</td></tr>
  <tr><td port="3">Measurements</td></tr>
  <tr><td port="4">Results</td></tr>
  <tr><td port="5">Input Type</td></tr>
  <tr><td port="6">Output Type</td></tr>
</table>>];

Results [label=<
<table border="0" cellborder="1" cellspacing="0">
  <tr><td><b>Results</b></td></tr>
  <tr><td port="1">Results ID</td></tr>
  <tr><td port="2">Results</td></tr>
  <tr><td port="2">Visuals</td></tr>
</table>>];


Calculations -> Calculations
Submissions:3 -> Calculations:5;
Calculations:4 -> Results:2;
UserHistory:1 -> Results:1;
Users:1 -> Submissions:1;
Users:1 -> UserHistory:2;
}
