
# Job Interview Test Answers

## CORS

### 1. What does CORS stand for and why was it introduced?
**Answer:**
CORS stands for Cross-Origin Resource Sharing. It was introduced to allow or restrict web pages from making requests to a different domain than the one that served the initial web page, enabling secure cross-domain requests and data transfers between browsers and web servers.

### 2. Explain what typically causes CORS errors when developing web applications.
**Answer:**
CORS errors typically occur when a web page tries to make a request to a different domain, protocol, or port from its own. The browser blocks these requests for security reasons unless the other domain explicitly allows them via CORS headers.

### 3. Describe a situation where you might encounter CORS errors and how you would resolve them.
**Answer:**
A common situation is when a frontend application hosted on one domain (e.g., `example.com`) tries to access resources from another domain (e.g., `api.example.com`). To resolve this, the server at `api.example.com` needs to include the appropriate CORS headers, like `Access-Control-Allow-Origin: http://example.com`, in its responses.

### 4. What is a preflight request in the context of CORS? How does it work?
**Answer:**
A preflight request is a CORS request that checks to see if the CORS protocol is understood. It uses the `OPTIONS` method to send headers that indicate what HTTP methods and headers are allowed for a subsequent actual request.

### 5. What constitutes a simple request in CORS? Give an example.
**Answer:**
A simple request in CORS is one that meets certain criteria that allows it not to trigger a preflight. Examples include using HTTP methods GET, HEAD, or POST, and Content-Type of `text/plain`, `multipart/form-data`, or `application/x-www-form-urlencoded`. Example: A GET request for a resource that doesn't require custom headers.

## Git

### 1. What is Git and how does it work under the hood?
**Answer:**
Git is a distributed version control system that manages and stores revisions of projects. Under the hood, Git uses a series of snapshots of your files. These snapshots are committed into your local repository and can be shared and merged with other repositories.

### 2. Describe what a branch is in Git and how it can be created.
**Answer:**
A branch in Git is essentially a pointer to a snapshot of your changes. When you want to add new features or fix bugs, you can create new branches and switch between them. It is created with `git branch <branch_name>` or `git checkout -b <branch_name>`.

### 3. What happens when you delete a branch? Is there a way to recover it?
**Answer:**
When you delete a branch, you're removing that specific pointer. However, the commits themselves remain in the repository until they're pruned or garbage collected. You can recover a deleted branch if you know the commit hash by creating a new branch pointing to that hash.

### 4. Explain the Git commands listed.
**Answer:**
- `git checkout -b mybranch`: Creates and switches to a new branch named `mybranch`.
- `git add passwords.txt`: Stages the file `passwords.txt` for the next commit.
- `git commit -m "added passwords"`: Commits the staged files with the message "added passwords".
- `git push origin mybranch`: Pushes `mybranch` to the remote repository `origin`.
- `git push -f origin mybranch`: Forcibly pushes `mybranch` to the remote, potentially overwriting changes.

### 5. How can you view the list of branches in a local repository using command line?
**Answer:**
You can view the list of branches in a local repository by running `git branch` or `git branch --list`. For remote branches, use `git branch -r`.

## JavaScript / TypeScript

### 1. Analyze the following JavaScript code snippet and explain what it does.
**Code:**
```javascript
const state = undefined;
const a = 0;
console.log(a || alert('bar'));
```
**Answer:**
This code snippet uses the logical OR operator to check the value of `a`. Since `a` is `0` (a falsy value), it executes `alert('bar')`, which shows an alert with "bar". The `console.log` outputs `undefined` because `alert()` does not return any value.

### 2. What is the output of this code and why?
**Answer:**
The output in the console is `undefined` because `alert('bar')` does not return a value, and the

 `alert` function's execution does not produce a return value to be logged by `console.log`.

### 3. Discuss the use of logical operators in JavaScript with examples.
**Answer:**
Logical operators in JavaScript (`&&`, `||`, `!`) are used to perform Boolean operations. For example, `a && b` returns `b` if `a` is true, and `a` if it is false. `a || b` returns `a` if it is true, and `b` if `a` is false. `!a` inverts the Boolean value of `a`.

## Debugging

### 1. Estimate the time needed to identify a commit causing performance degradation using binary search.
**Answer:**
With 1024 commits and each test taking 5 minutes, using a binary search method would take log2(1024) * 5 = 50 minutes, as binary search halves the dataset each step.

### 2. Explain the binary search approach to debugging. Why is it efficient?
**Answer:**
Binary search in debugging is efficient because it continuously splits the range of commits in half to quickly isolate the problematic commit. This reduces the number of steps significantly compared to linear search.

### 3. What are some other strategies you might use besides going through git commits?
**Answer:**
Other strategies include code profiling to identify slow functions, using debuggers to step through code execution, and adding logging statements to understand the state and flow of the application.

---

This document provides detailed answers and explanations tailored for a job interview scenario, focusing on the key areas of knowledge you specified.
