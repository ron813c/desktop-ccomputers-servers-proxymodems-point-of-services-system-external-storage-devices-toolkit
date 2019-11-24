#lighthouse install on Android with termux using yarn, npm, gzip, and git
[1] INSTALLATION YARN ON TERMUX  Step Format
start by running
"pkg install yarn"
next run
apt-get upgrade-yarn
next run
pkg install npm
next run
pkg upgrade-all
next run 
"pkg install gzip"
next step
pkg install git 
apt-get upgrade

LIGHTHOUSE CHANNELING INSTALLATION WORK AROUND PROCESS
Example
yarn add JSON
{
  "name": "custom-lighthouse-recipe",
  "private": true,
  "scripts": {},
  "devDependencies": {
    "lighthouse": "^5.6.0"
  }
}


NEXT EXAMPLE
yarn add JSON

yarn add JSON








const lighthouse = require('lighthouse');
const chromeLauncher = require('chrome-launcher');

function launchChromeAndRunLighthouse(url, opts, config = null) {
  return chromeLauncher.launch({chromeFlags: opts.chromeFlags}).then(chrome => {
    opts.port = chrome.port;
    return lighthouse(url, opts, config).then(results => {
      // use results.lhr for the JS-consumeable output
      // https://github.com/GoogleChrome/lighthouse/blob/master/types/lhr.d.ts
      // use results.report for the HTML/JSON/CSV output as a string
      // use results.artifacts for the trace/screenshots/other specific case you need (rarer)
      return chrome.kill().then(() => results.lhr)
    });
  });
}

const opts = {
  chromeFlags: ['--show-paint-rects']
};
͝�6��;�G�_1Rn�EKd�
_����
//custom-config.js

module.exports = {
  extends: 'lighthouse:default',
  settings: {
    onlyAudits: [
      'first-meaningful-paint',
      'speed-index',
      'first-cpu-idle',
      'interactive',
    ],
  },
};
CLI

lighthouse --config-path=path/to/custom-config.js https://example.com
Node

const lighthouse = require('lighthouse');
const config = require('./path/to/custom-config.js');
lighthouse('https://example.com/', {port: 9222}, config);
Properties
Name	Type
extends	string|boolean|undefined
settings	Object|undefined
passes	Object[]
audits	string[]
categories	Object|undefined
groups	Object|undefined
extends: string|boolean|undefined
//Example
{
  extends: 'lighthouse:default',
//network throttling and audit whitelisting/blacklisting.
{
  settings: {
    onlyCategories: ['performance'],
    onlyAudits: ['works-offline'],
{ "name": "custom-lighthouse-recipe", "private": true, "scripts": {}, "devDependencies": { "lighthouse": "^5.6.0" 
{
  passes: [
    {
      passName: 'fastPass',
      gatherers: ['fast-gatherer'],
    },
    {
      passName: 'slowPass',
      recordTrace: true,
      useThrottling: true,
      networkQuietThresholdMs: 5000,
      gatherers: ['slow-gatherer'],
{
  audits: [
    'first-meaningful-paint',
    'first-cpu-idle',
    'byte-efficiency/uses-optimized-images',
  ]
{
  categories: {
    performance: {
      title: 'Performance',
      description: 'This category judges your performance',
      auditRefs: [
        {id: 'first-meaningful-paint', weight: 2, group: 'metrics'},
        {id: 'first-cpu-idle', weight: 3, group: 'metrics'},
        {id: 'interactive', weight: 5, group: 'metrics'},
      ],
{
  categories: {
    performance: {
      auditRefs: [
        {id: 'my-performance-metric', weight: 2, group: 'metrics'},
      ],
    }
  },
  groups: {
    'metrics': {
      title: 'Metrics',
      description: 'These metrics encapsulate your web app\'s performance across a number of dimensions.'
       lighthouse-core/config/default-config.js
lighthouse-core/config/lr-desktop-config.js
lighthouse-core/config/lr-mobile-config.js
lighthouse-core/config/perf-config.js
lighthouse-core/config/mixed-content-config.js
docs/recipes/custom-audit/custom-config.js
pwmetrics{
   }
};
iy���]�D��V�y�p��P�2@��IY

yarn add JSON

// Usage:
launchChromeAndRunLighthouse('https://example.com', opts).then(results => {
  // Use results!
});
 desktop-ccomputers-servers-proxymodems-point-of-services-system-external-storage-devices-toolkit

git clone https://github.com/users/set_protocol?protocol_selector=ssh&protocol_type=clone% module load gcc/6.1.1
% which gcc
/usr/local/gcc/6.1.1/linux-x86_64/bin/gcc

Now we'll switch to a different version of the module

% module switch gcc gcc/6.3.1
% which gcc
/usr/local/gcc/6.3.1/linux-x86_64/bin/gcc

And now we'll unload the module altogether

% module unload gcc
% which gcc

Now we'll log into a different machine, using a different shell (tcsh).

tardis-> module load gcc/6.3.1
tardis-> which gcc
git clone https://usr/local/gcc/6.3.1/linux-aarch64/bin/gcc

git clone https://github.com/GoogleChrome/lighthouse.gitconst lighthouse = require('lighthouse');
const chromeLauncher = require('chrome-launcher');

function launchChromeAndRunLighthouse(url, opts, config = null) {
  return chromeLauncher.launch({chromeFlags: opts.chromeFlags}).then(chrome => {
    opts.port = chrome.port;
    return lighthouse(url, opts, config).then(results => {
      // use results.lhr for the JS-consumeable output
      // https://github.com/GoogleChrome/lighthouse/blob/master/types/lhr.d.ts
      // use results.report for the HTML/JSON/CSV output as a string
      // use results.artifacts for the trace/screenshots/other specific case you need (rarer)
      return chrome.kill().then(() => results.lhr)
    });
  });
}

const opts = {
  chromeFlags: ['--show-paint-rects']
};

// Usage:
launchChromeAndRunLighthouse('https://example.com', opts).then(results => {
  // Use results!
});
