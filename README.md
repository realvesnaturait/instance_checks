![instance-scan-check-banner](https://github.com/Lacah/example-instancescan-checks/assets/47461634/2dc8c308-a249-41ca-89f6-26bc68749f7c)

# example-instancescan-checks
 
Open-Sourced community contributed and owned repository for Instance Scan Definitions. [ServiceNow Instance Scan](https://docs.servicenow.com/csh?topicname=hs-landing-page&version=latest) The checks contained in this repository are therefore considered "use at your own risk" and will rely on the open-source community to help drive fixes and feature enhancements via Issues and community members issuing and reviewing PRs. ServiceNow is not providing or authenticating these definitions. Occasionally, ServiceNow employees may choose to contribute to the open-source project as members of the community as they see fit, this does not constitute a service or product from ServiceNow.

🔔🔔🔔<br>
***CONTRIBUTORS must follow all guidelines in [CONTRIBUTING.md](CONTRIBUTING.md)*** or run the risk of having your Pull Requests labeled as spam.<br>
🔔🔔🔔

# Checks in this repository

## Category: Manageability

| Name | Description |
|------|-------------|
| Inactive user check: Approvals | Check any approvals waiting in inactive users queue |
| Inactive user check: Catalog task Assigned To | Check any Catalog Tasks Assigned to Inactive user |
| Check any assets assigned to inactive user | Check if any asset is assigned to inactive users. |
| Check if any incidents are assigned to inactive users. | Check if any incidents are assigned to inactive user. |
| Inactive User Check: Catalog Item | We should ensure that inactive users are removed from being assigned as Catalog item owners. |
| Check problem ticket assigned to inactive user | Make sure that a problem ticket is not assigned to an inactive user. |
| Avoid gs.log() Statement | Use Logging Levels: Instead of gs.log(), consider using more appropriate logging levels, such as: gs.info() for informative messages. gs.warn() for warnings that don’t break functionality but may need attention. gs.error() for logging errors that require investigation. |
| Create ATFs in sub production instance | Highly recommended practice to use ATFs for regression testing on instance upgrade and releases. |
| Avoid using javascript "document" object in Portal | Always avoid using native js "document" object for DOM manipulation in service portal. Instead we should use AngularJS equivalent capabilities to achieve the same. |
| Don't use new Array() | In general, you should use the array literal notation when possible. It is easier to read, it gives the compiler a chance to optimize your code, and it's mostly faster too. |
| Corrupt CI Relationships | CI Relationship records without a parent or a child record should not exist. Such CI Relationship records technically won't function. Situations like these are likely to occur due to incorrect manual System Administrative duties or incorrect automated processes. |
| Scripts should not contain gs.log statements | The gs.log() statement can be used to write information to the system log. It is generally used when debugging. Using gs.log() statements will pollute the system log. Prior to promoting artifacts to a production instance, debugging statement should - in most cases - be removed. |
| Scripts should not contain gs.info statements | The gs.info() statement can be used to write information to the system log. It is generally used when debugging. Using gs.info() statements will pollute the system log. Prior to promoting artifacts to a production instance, debugging statement should - in most cases - be removed. |
| CMDB records with broken references | Reference fields are a stored reference to a field on another table. This creates a relationship between the two tables. In some cases, the reference gets broken. Technically the field will still hold a value, though will display a blank value or a sys_id and the reference does not work anymore. The reference is incorrect or worse, the reference does not exist on the target table (also not under an other sys_id). This could occur due to scripting, scripting with hardcoded incorrect values, imported data with incorrect references (for example sys_ids to references might differ between instances when those records were newly created instead of being promoted between the instances). |
| Many-to-many records with broken references | Reference fields are a stored reference to a field on another table. This creates a relationship between the two tables. In some cases, the reference gets broken. Technically the field will still hold a value, though will display a blanc value or a sys_id and the reference does not work anymore. The reference is incorrect or worse, the reference does not exist on the target table (also not under an other sys_id). This could occur due to scripting, scripting with hardcoded incorrect values, imported data with incorrect references (for example sys_ids to references might differ between instances when those records were newly created instead of being promoted between the instances). |
| Task records with broken references | Reference fields are a stored reference to a field on another table. This creates a relationship between the two tables. In some cases, the reference gets broken. Technically the field will still hold a value, though will display a blanc value or a sys_id and the reference does not work anymore. The reference is incorrect or worse, the reference does not exist on the target table (also not under an other sys_id). This could occur due to scripting, scripting with hardcoded incorrect values, imported data with incorrect references (for example sys_ids to references might differ between instances when those records were newly created instead of being promoted between the instances). |
| Consider using getXMLAnswer instead of getXML | getXMLAnswer only retrieves the Answer which we are actually after. getXML retrieves the whole XML document. In most cases, we are not interested in the whole XML document, though only in the Answer. |
| Could not verify Remote instance connection | Connection test for the remote instance defined did not result in a positive response. |
| Duplicate Script Include Name | This uses a table check to find other Script Includes having the same API name. Technically this is possible, but causes issues as there is no way to control which Script Include will be instantiated when being called. |
| Don't use new Object() | In general, you should use the object literal notation when possible. It is easier to read, it gives the compiler a chance to optimize your code, and it's mostly faster too. |
| High number of workflows running for a single record | In general, for a single record only a few Workflow context will be running. If a high number of Workflow context are active, this often indicates an issue on the starting conditions of your Workflow. More then 10 active Workflow context is considered being a high number. |
| Parent All Nodes/Active Nodes without childs | Schedule records with system ID "all Nodes" or "active nodes", are considered to be parent schedules. Parent schedules that themselves will never run but instead spawn child jobs (of the same name) for each application node required by their definition. |
| Product Catalog without Product Models | Catalog Items in the Product Catalog should be created from the underlying Product Model and this association should be kept intact. |
| Scripts should not contain debugging statements in production | The "gs.log()", "gs.debug()", "console.log()", etc. statements can be used to write information to the system log. |
| Unprocessed queues | External Communication Channel (ECC) Queue is a connection point between an instance and the MID Server. Jobs that the MID Server needs to perform are saved in this queue until the MID Server is ready to handle them. |
| Unprocessed schedules | Schedules with a state "Ready" run at the next scheduled interval. |
| Do not use hard-coded sys_ids | Hard-coded sys_ids can lead to unpredictable results (sys_ids may differ between instances) and can be difficult to track down. |
| Hard coded Instance URL | Hard coding instance URL is not a best practice as they reduce the usability of your code. |
| Before Business rules should not insert() records in any tables | Before business rules execute before the data on current record is saved to database. |
| Update set description should not be empty | Validates the description of the update sets created is not empty as it provides the release management team better understanding what's getting pushed. |
| Update set should not have more than 1000 updates | Update sets with more than 1000 configuration updates should be broken down into multiple update sets with batching or the parent story has to be more granular. |
| Updates in wrong update set scope | The scope for Customer Update records should match the scope of the Update Set in which the Customer Update resides. |
| Duplicate Updat Set Name | Maintain unique names for update set names it will help to track the updates easyly and also very useful to debug any issues. |
| Delete orphaned variables | Variables should be used in Catalog Item or a Variable Set. Variables not in use should be deleted. |
| Delete Orphaned Catalog Client Scripts | Catalog Client Script should be used in either a Catalog Item or a Variable Set. Catalog Client Scripts not in use should be deleted. |
| Delete Orphaned Catalog UI Policies | Catalog UI policy should be used in either a Catalog Item or a Variable Set. Catalog UI Policies not in use should be deleted. |
| Client Script Business rule or Script Include should not have an empty description or be without comments in the script section | Comments and description add extra information int he scripts and usally help in long run and during upgrades if an udate has been made so its a best practice to add comments and a description to these platform scripts. |
| Active groups without active users | Groups are commonly used in business process for approvals, and notifications. Avoiding groups that are empty, or contain only inactive users, can cause processes to halt or provide unexpected results. |
| Valid Script Include Name - No Spaces | Script Includes names should not include spaces since it is not possible to call them if there is a space in the name. |
| Roles assigned to non-existing users | Identify role assignments (sys_user_has_role) for users that do not exists |
| Assign roles to Group | Assign Roles to sys_user_group , Rather than assigning roles to sys_user , It becomes difficult while adding lot of roles |
| Check the incidents that are closed or canceled but still active | This is a table check on the incidents table that verifies if there are closed or canceled incidents in the active state |
| Open Requests with closed requested items | If all the requested items in a request are closed, the request should close automatically. |
| Integration users shouldn't be admin | Finds integration users that have assigned admin role |
| Update set In Progress previously completed | Already completed Update Set shouldn't be set back to In Pogress |
| Active notifications with empty any recipients class | Active notifications where all the three classes of recipients can be empty |
| Dashboard Onwer no longer active | For the dashboard there should be an active owner |
| Unsupported API GlideLDAP | GlideLDAP API usage is unsupported by ServiceNow |
| Check for Orphaned Tickets | Tickets from tables such as Incident, Change Request, Problem, and other task-related tables should always have an Assignment Group specified. |
| Check Inactive Business Rules over 90 days | Inactive Business Rules which are not updated for more than 90 days |
| Update set In Progress/Completed previously Ignored | Usually, developers mark an updatesets as Ignore |



## Category: Upgradability

| Name | Description |
|------|-------------|
| Call GlideRecord using new | Good naming convention and self-descriptive code contain "new" to define GlideRecord. In some versions or for some parts of the Platform leaving "new" off will work, though for other parts of the Platform or after upgrades this can cause unexpected behavior. |
| Incident table should not be extended | Check if the baseline restriction to extend the Incident table has been removed and at least one child table extending Incident has been created. |
| Choice table should not be extended | Check if the Choice [sys_choice] table has been extended. This is not supported by ServiceNow. |
| User table should not be extended | Check if the User [sys_user] table has been extended. This is not recommended and can cause problems when a user needs to be in more than one user table. |
| Do not reference sys_choice table | The Choice table should not be used as the reference table for a Reference type field. Reference fields store the sys_id of the corresponding record in the reference table and show the specified display value. |


## Category: Performance

| Name | Description |
|------|-------------|
| Identifies string fields with max_length exceeding recommended limits | This scan checks for string fields where the max_length value is set above a recommended limit. Setting a very high max_length can result in unnecessary database storage consumption and may degrade query performance. It is important to use reasonable max_length values based on actual data requirements. |
| getMessage() called in Client Script | This is a simple table check to find client scripts with use the getMessage function but do not preload messages using the Messages field. As the check does a simple contains query it could produce false-positives if the getMessage is either commented or from another library. |
| Glide-API in ACL | This will check ACL rules with operation READ for usage of Glide API calls, i.e. GlideRecord and GlideAggregate as these can cause significant performance impact. s the check does a simple contains query it could produce false-positives if the getMessage is either commented or from another library. |
| Cache flushed as part of scripts | This is using some advanced linter check to find usages of gs.setProperty or gs.cacheFlush. Both functions will trigger a cache flush and thus cause performance impacts. |
| Global Business Rules | This is a simple table check to find Business Rules that are global. Global Business Rules have no condition or table restrictions and load on every page in the system. Most functions defined in global Business Rules are fairly specific. |
| Global Client Scripts | This is a simple table check to find Client Scripts that are global. Global client scripts have no table restrictions; therefore they will load on every page in the system introducing browser load delay in the process. |
| Using Synchronous AJAX calls in client script | Synchronous usage of AJAX calls (getXMLWait) pauses the browser interaction until data is retrieved from the server side and thereby reducing user experience. |
| Business Rule without any conditions | A business rule is triggered whenever a user opens a list or form view or when a user inserts/updates or deletes a record. Without any conditions added, it will always evaluate to true. |
| Business rules should not use current.update() | Avoid using current.update() in a business rule script. The update() method triggers business rules to run on the same table. |
| Avoid Dot-Walking to the sys_id of a Reference Field | The value of a reference field is a sys_id. When you dot-walk to the sys_id, the system does an additional database query. |
| Do not use getRowCount() for fetching row count | Using getRowCount method of GlideRecord can cause performance issues while quering on tables with high record count. |
| Query business rules should not use query() on GlideRecord | Query business rules that query themselves will continue to loop indefinitely until being caught by the platforms recursion limit. |
| Always deregister $rootScope.$on listeners on the scope $destory event | $rootScope.$on listeners will remain in memory if not properly cleaned up. This will create a memory leak if the controller falls out of scope. |
| Provide alternate value when fetching Glide property | Recommendation to provide alternate/default value when calling gs.getProperty() to avoid errors if the property is not set. |
| Using setValue()'s displayValue Parameter with Reference Fields | When using setValue() on a reference field, be sure to include the display value with the value (sys_id). |
| Running Business Rules on Transform Maps | Running business rules during transform may cause the transform to take longer than expected. |
| Avoid using getReference() | getReference is no longer considered best practice due to its performance impact. |
| Restrict rowcount to 10,20,50 max from user preference table | Restrict the number of row counts max to 10,20,50 instead of higher limits such as 100 and 1000. |
| Instance scan check to identify slow jobs in transaction logs. | The Instance Scan Check is a table check scan that allows administrators to investigate transaction logs in ServiceNow to diagnose performance issues reported by users. |
| Check System Property with 'Ignore cache' = False | Ignore Cache is a Glide Properties field that impacts system performance. |
| Avoid using gs.sleep() in any server-side script | Avoid using gs.sleep() in any script because it does not release session and will cause delays. |


## Category: Security

| Name | Description |
|------|-------------|
| Check Mandatory fields on incident | This check is used to find mandatory fields on incident |
| Avoid using setBasicAuth for REST messages | It is possible to script REST messages directly. Using the .setBasicAuth method is considered a security risk. |
| Tables without ACLs | This check searches for any custom table if there exists at least one ACL record. |
| Scripted REST API without Authentication | Scripted REST APIs should be not be public but enforce access controls. |
| Avoid the eval function | Improper use of eval() opens up your code for injection attacks. |
| Do not use gr as a variable name | The platform is Javascript and a lot of code is run in a global variable scope. |
| Admins not logged in for 1 month | Monitor users with role admin that are not logged for longer than 1 month |
| Users left in already inactivated Groups | After deactivation of Groups there can be still some users. |
| Report with public role can expose data | It is possible that reports are accessible with public role. |
| Scheduled Job with RunAs set as Locked Out user | Detecting no longer active user set as RunAs for Scheduled Job |
| Client Scripts should not use GlideRecord() API | Verify that instance doesn't have GlideRecord usage in client scripts |
| Inactive users should be also locked out | If the user is deactivated he should also be locked out |
| Employee files should not be cloned over to sub production instances. | Verify that clone exclude table configuration contains HR tables |
| Workflow context table has an active record for more than 6 months | Active workflows consume DB space and impact performance |
| Flow context table has an active record for more than 6 months | Review flow contexts running for more than 6 months |
| Active users with past employment end date | Review users whose employment end date is in the past |
| Set glide.invalid_query.returns_no_rows to true | When this property does not exist an invalid query will return all rows |
| Use GlideRecordSecure instead of GlideRecord API for Client Callable Script Include | Use GlideRecordSecure API to ensure the security checks are performed |
| For loop iterators "i" should be declared | Variables in JavaScript should be properly declared |
| Don't show unpublished knowledge articles | Unpublished knowledge articles may contain sensitive information |
| Scripts in ACLs should be cleared when Advanced is not checked | Scripts in ACLs are executed regardless of Advanced checkbox |


## Category: User Experience

| Name | Description |
|------|-------------|
| Added a Number Prefix which already exists | Creating new number records does not require uniqueness. |
| List Inactive users from active group | List inactive users that still belongs to activate groups |
| HTTP connection records not excluded on clones from Prod | Orphaned http_connection records after clone |
| Avoid using alert() in client scripts | It is recommended to use an OOB library for modals |
| Use "last run datetime" for JDBC data loads | Ensure incremental data loading |
| Use of setWorkflow(false) in business rules will cause unexpected issues | setWorkflow(false) can skip execution of business rules |
| Make use of isLoading Check (onChange Client Scripts Only) | Prevent unnecessary code execution |
| Make sure columans are selected in list type reports | It is recommended to select columans in List type report |
| Find Orphaned UI Policies | Orphaned UI policies add technical debt |



# Additional resources

Please check these additional links for more information and details:

- [Platform Academy Foundation #5: Instance Scan Overview](https://community.servicenow.com/community?id=community_event&sys_id=f44eb0c0db82f410019ac22305961950)
- [Mark Roethof’s Blogs](https://community.servicenow.com/community?id=community_blog&sys_id=14e51965db2200d013b5fb24399619fb#is)
- [Live Coding Happy Hour – Instance Scan in Quebec (2021-03-12)](https://youtu.be/_cPlWnh1Z68)
- [Introduction to ServiceNow HealthScan and Instance Scan](https://nowlearning.service-now.com/lxp?id=overview&sys_id=e4c538231b0d6c505b2699f4bd4bcb6f&type=course)
- [K21 CCL1062 – Writing custom instance scan checks](https://nowlearning.servicenow.com/lxp/en/now-platform/introduction-to-servicenow-healthscan-and-instance-scan?id=learning_course_prev&course_id=fc3014c5db728150a87c2d3d569619d5)
- [Quebec Instance Scan](https://developer.servicenow.com/blog.do?p=/post/quebec-instancescan/)
