# JavaScript-Domain-Extracter

function domainName(domain) {
  const a = document.createElement('a');
  a.href = domain;
  const { hostname } = a;
  const hostSplit = hostname.split('.');
  hostSplit.pop();
  if (hostSplit.length > 1) {
    hostSplit.shift();
  }
  return hostSplit.join();
}
test

---------------------------
domainName("http://google.com")
