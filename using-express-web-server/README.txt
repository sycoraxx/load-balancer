npm init -y
npm i express axios
npm i concurrently -g

## Create two file config.js for the load balancer server and index.js for the application server.

Explanation:
------------
The above code starts with 2 Express apps, one on port 3000 and another on port 3001. The separate load balancer process should alternate between these two, sending one request to port 3000, the next request to port 3001, and the next one back to port 3000.

Execution (in current directory):
--------------------------------

concurrently "node config.js" "node index.js" 