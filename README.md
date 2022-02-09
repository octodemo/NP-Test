# GHAS Demo Repository

This demo repo will allow you to demo Advanced Security features and functionality from the perspective of the developer.

The following repository contains vulnerability [CVE-2018-20835](https://github.com/advisories/GHSA-x2mc-8fgj-3wmr) (aka Zip Slip) that was found by the [GitHub Security Lab](https://securitylab.github.com/).

You will be able to generate a Pull Request and show the discovery of a vulnerability inside a PR.

## Demo flow

<details>
<summary>Copy this template</summary>
<p> 
  
Begin by [using this template repo](https://github.com/octodemo/template-ghas-demo/generate).
</p>
</details>

<details>
<summary>Run GitHub Action: Setup - Create Vulnerable Branch </summary>
<p> 

#### Actions tab

Click on the `Actions` tab.

<img src="https://user-images.githubusercontent.com/62304682/130997001-2336f7b3-087d-40b3-b2b6-c815aa2e91d7.png" width="70%"/>

#### Run `Setup - Create Vulnerable Branch`

Click `Run Workflow`.

Keep default values.

<img src="https://user-images.githubusercontent.com/62304682/130997100-6ffea0ed-e58c-41da-aec8-d3321637d40e.png" width="70%"/>

This will create a new branch, move files from the folder `Feature-Vulnerable-Content`, and rename the file types.
</p>
</details>

<details>
  
<summary>Create Pull Request</summary>
<p>

Click on the `Pull Requests` tab.

Create a new pull request from the newly created branch to the main branch:

<img src="https://user-images.githubusercontent.com/62304682/130997949-906ca5e1-5755-4811-b8f1-6b41cd107436.png" width="70%"/>


#### View Workflow Run 

Note that a GitHub Action has been triggered on the pull request `CodeQL / Analyze (javascript) (pull_request) `

<img src="https://user-images.githubusercontent.com/62304682/130998598-fcfdc53e-f683-4eb9-9e2c-f4cc46245026.png" width="70%"/>

</p>
</details>

<details>
<summary>GitHub Actions Progress</summary>

<p>
 
#### GitHub Actions Progress

Click `Actions` tab -> `CodeQL`

Click the specific workflow run. You can view the progress of the Workflow run until the analysis completes.

<img src="https://user-images.githubusercontent.com/6920330/96748337-64f99600-1397-11eb-9ab7-b78ec23466ae.png" width="80%"/>

</p>
</details>

<details>
<summary>Security Issues</summary>
<p>
  
Once the Workflow has completed, check the pull request and viewed the failed status check -> ` Code scanning results / CodeQL `. This will include `2 new alerts`. Click the `Details` option

<img src="https://user-images.githubusercontent.com/62304682/130999726-7274061c-a43d-4bb1-b46e-2f842b7f8f7f.png" width="80%"/>


#### Code scanning results View

Walk through the discovered vulnerabilities:

<img src="https://user-images.githubusercontent.com/62304682/130999949-04bcdd6d-c343-4d2f-b74f-1f929889679b.png" width="80%"/>

#### Show Paths Button

CodeQL Analysis is able to trace the dataflow path from source to sink and gives you the ability to view the path traversal within the alert.

Click `show paths` in order to see the dataflow path that resulted in this alert.

<img src="https://user-images.githubusercontent.com/62304682/131000369-961cd80c-f700-4a4d-8b9f-736eb0e54f82.png" width="80%"/>

#### Show Paths View

<img src="https://user-images.githubusercontent.com/6920330/96749909-6926b300-1399-11eb-99df-143d17804aeb.png" width="80%"/>

</p>
</details>
