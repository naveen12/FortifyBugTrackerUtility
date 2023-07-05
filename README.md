# FortifyBugTrackerUtility

Introduction
====
The Maven projects in this repository make up a utility for submitting vulnerabilities from Fortify on Demand (FoD) 
and Fortify Software Security Center (SSC) to bug trackers and other external systems. The following table
lists the currently supported functionalities.

| Target System | From FoD | From SSC | Grouping | State Management | Remarks |
| ------------- | -------- | -------- |--------- | ---------------- | ------- |
| RSA Archer    | Yes      | Yes      | No       | No               | Currently only supports text and value list field types |
| CSV File      | Yes      | Yes      | No       | No               | By default, a separate output file is written for each application version/release. All relevant vulnerabilities are exported on each run, overwriting any existing files |
| Atlassian Jira | Yes     | Yes      | Yes      | Yes              | |
| ALM Octane     | Yes     | Yes      | Yes      | Yes              | |
| Azure DevOps  | Yes     | Yes      | Yes      | Yes              | Additional state transitions may need to be configured |
| SSC Bug Trackers | No    | Yes      | Yes      | Performed by SSC | Sample configuration for SSC Jira bug tracker included, other SSC bug trackers require corresponding configuration files to be added |

For more information about configuring and running the utility, please see the documentation included with the [binary distribution](https://github.com/fortify-ps/FortifyBugTrackerUtility/releases).

Note: Builded files added here, if you want your own then follow below steps

Building the project
----
Once all prerequisites have been met, you can use the following commands to build this project:

* `git clone https://github.com/fortify-ps/FortifyBugTrackerUtility.git`
* `cd FortifyBugTrackerUtility`
* `git checkout [branch or tag that you want to build]`
* `mvn clean package`

Once completed, build output like executable JAR file, sample configuration files, and the 
binary distribution zip file, can be found in the bugtracker/target directory.


# Licensing

See [LICENSE.TXT](LICENSE.TXT)

