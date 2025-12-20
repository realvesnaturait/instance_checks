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
| CMDB records with broken references | Reference fields are a stored reference to a field on another table. This creates a relationship between the two tables. In some cases, the reference gets broken. Technically the field will still hold a value, though will display a blank value or a sys_id and the reference does not work anymore. |
| Many-to-many records with broken references | Reference fields are a stored reference to a field on another table. This creates a relationship between the two tables. In some cases, the reference gets broken. Technically the field will still hold a value, though will display a blanc value or a sys_id and the reference does not work anymore. |
| Task records with broken references | Reference fields are a stored reference to a field on another table. This creates a relationship between the two tables. In some cases, the reference gets broken. Technically the field will still hold a value, though will display a blanc value or a sys_id and the reference does not work anymore. |
| Consider using getXMLAnswer instead of getXML | getXMLAnswer only retrieves the Answer which we are actually after. getXML retrieves the whole XML document. |
| Could not verify Remote instance connection | Connection test for the remote instance defined did not result in a positive response. |
| Duplicate Script Include Name | This uses a table check to find other Script Includes having the same API name. Technically this is possible, but causes issues as there is no way to control which Script Include will be instantiated when being called. |
| Don't use new Object() | In general, you should use the object literal notation when possible. It is easier to read, it gives the compiler a chance to optimize your code, and it's mostly faster too. |
| High number of workflows running for a single record | In general, for a single record only a few Workflow context will be running. More then 10 active Workflow context is considered being a high number. |
| Parent All Nodes/Active Nodes without childs | Schedule records with system ID "all Nodes" or "active nodes", are considered to be parent schedules. |
| Product Catalog without Product Models | Catalog Items in the Product Catalog should be created from the underlying Product Model and this association should be kept intact. |
| Scripts should not contain debugging statements in production | The "gs.log()", "gs.debug()", "console.log()", etc. statements can be used to write information to the system log. |
| Unprocessed queues | External Communication Channel (ECC) Queue is a connection point between an instance and the MID Server. |
| Unprocessed schedules | Schedules with a state "Ready" run at the next scheduled interval. |
| Do not use hard-coded sys_ids | Hard-coded sys_ids can lead to unpredictable results and can be difficult to track down. |
| Hard coded Instance URL | Hard coding instance URL is not a best practice as they reduce the usability of your code. |
| Before Business rules should not insert() records in any tables | Before business rules execute before the data on current record is saved to database. |
| Update set description should not be empty | Validates the description of the update sets created is not empty. |
| Update set should not have more than 1000 updates | Update sets with more than 1000 configuration updates should be broken down into multiple update sets. |
| Updates in wrong update set scope | The scope for Customer Update records should match the scope of the Update Set. |
| Duplicate Updat Set Name | Maintain unique names for update set names it will help to track the updates easyly. |
| Delete orphaned variables | Variables should be used in Catalog Item or a Variable Set. |
| Delete Orphaned Catalog Client Scripts | Catalog Client Script should be used in either a Catalog Item or a Variable Set. |
| Delete Orphaned Catalog UI Policies | Catalog UI policy should be used in either a Catalog Item or a Variable Set. |
| Client Script Business rule or Script Include should not have an empty description or be without comments in the script section | Comments and description add extra information in the scripts. |
| Active groups without active users | Groups are commonly used in business process for approvals, and notifications. |
| Valid Script Include Name - No Spaces | Script Includes names should not include spaces. |
| Roles assigned to non-existing users | Identify role assignments for users that do not exists |
| Assign roles to Group | Assign Roles to sys_user_group , Rather than assigning roles to sys_user |
| Check the incidents that are closed or canceled but still active | This is a table check on the incidents table that verifies invalid state combinations. |
| Open Requests with closed requested items | If all the requested items in a request are closed, the request should close automatically. |
| Integration users shouldn't be admin | Finds integration users that have assigned admin role |
| Update set In Progress previously completed | Already completed Update Set shouldn't be set back to In Pogress |
| Active notifications with empty any recipients class | Active notifications where all recipient classes are empty |
| Dashboard Onwer no longer active | For the dashboard there should be an active owner |
| Unsupported API GlideLDAP | GlideLDAP API usage is unsupported by ServiceNow |
| Check for Orphaned Tickets | Tickets should always have an Assignment Group specified |
| Check Inactive Business Rules over 90 days | Inactive Business Rules which are not updated for more than 90 days |
| Update set In Progress/Completed previously Ignored | Ignored update sets reused for active work |


## Category: Upgradability

| Name | Description |
|------|-------------|
| Call GlideRecord using new | Good naming convention and self-descriptive code contain "new" to define GlideRecord. In some versions or for some parts of the Platform leaving "new" off will work, though for other parts of the Platform or after upgrades this can cause unexpected behavior. |
| Incident table should not be extended | Check if the baseline restriction to extend the Incident table has been removed and at least one child table extending Incident has been created. |
| Choice table should not be extended | Check if the Choice [sys_choice] table has been extended. This is not supported by ServiceNow. |
| User table should not be extended | Check if the User [sys_user] table has been extended. This is not recommended and can cause problems when a user needs to be in more than one user table. |
| Do not reference sys_choice table | The Choice table should not be used as the reference table for a Reference type field. Reference fields store the sys_id of the corresponding record in the reference table and show the specified display value. For example: the caller_id field stores the sys_id of a record from the user table and displays the corresponding name value. This presents a problem when using the sys_choice table, because existing records are deleted and replaced when choices are modified. This causes a new sys_id to be generated for each record in the choice list. So the sys_id stored in the Reference field is no longer a valid value and the reference is broken. |


## Category: Performance

| Name | Description |
|------|-------------|
| Identifies string fields with max_length exceeding recommended limits | This scan checks for string fields where the max_length value is set above a recommended limit. |
| getMessage() called in Client Script | Client scripts using getMessage without preloading messages |
| Glide-API in ACL | ACL rules with READ operation using GlideRecord or GlideAggregate |
| Cache flushed as part of scripts | Usage of gs.setProperty or gs.cacheFlush |
| Global Business Rules | Business Rules that are global and load on every page |
| Global Client Scripts | Client Scripts that load on every page |
| Using Synchronous AJAX calls in client script | Synchronous usage of AJAX calls (getXMLWait) |
| Business Rule without any conditions | Business rules without conditions execute every time |
| Business rules should not use current.update() | Avoid recursive business rule execution |
| Avoid Dot-Walking to the sys_id of a Reference Field | Dot-walking to sys_id causes additional DB queries |
| Do not use getRowCount() for fetching row count | getRowCount causes performance issues on large tables |
| Query business rules should not use query() on GlideRecord | Query business rules querying themselves |
| Always deregister $rootScope.$on listeners | Prevent memory leaks in Service Portal |
| Provide alternate value when fetching Glide property | Provide default value in gs.getProperty |
| Using setValue()'s displayValue Parameter with Reference Fields | Avoid synchronous Ajax calls |
| Running Business Rules on Transform Maps | Business rules during transform slow down imports |
| Avoid using getReference() | getReference is no longer considered best practice |
| Restrict rowcount to 10,20,50 max | Restrict row count for better performance |
| Instance scan check to identify slow jobs | Identify transactions with response time > 120 seconds |
| Check System Property with 'Ignore cache' = False | Ignore cache impacts system-wide performance |
| Avoid using gs.sleep() in any server-side script | gs.sleep blocks sessions |

## Category: Security

| Name | Description |
|------|-------------|
| Check Mandatory fields on incident | This check is used to find mandatory fields on incident |
| Avoid using setBasicAuth for REST messages | Using setBasicAuth is considered a security risk |
| Tables without ACLs | Custom tables without any ACL |
| Scripted REST API without Authentication | Scripted REST APIs should enforce access controls |
| Avoid the eval function | Improper use of eval opens injection risks |
| Do not use gr as a variable name | gr can clobber global variables |
| Admins not logged in for 1 month | Monitor inactive admin users |
| Users left in already inactivated Groups | Users remaining in inactive groups |
| Report with public role can expose data | Reports accessible with public role |
| Scheduled Job with RunAs set as Locked Out user | Scheduled jobs using locked-out users |
| Client Scripts should not use GlideRecord() API | Use GlideAjax instead |
| Inactive users should be also locked out | Prevent Table API access |
| Employee files should not be cloned | Prevent HR data exposure |
| Workflow context table has active record > 6 months | Active workflows consume DB space |
| Flow context table has active record > 6 months | Stalled flow executions |
| Active users with past employment end date | Potential security threat |
| Set glide.invalid_query.returns_no_rows to true | Prevent unintended full-table queries |
| Use GlideRecordSecure instead of GlideRecord API | Enforce ACL checks |
| For loop iterators "i" should be declared | Prevent variable pollution |
| Don't show unpublished knowledge articles | Prevent exposure of sensitive content |
| Scripts in ACLs should be cleared when Advanced is not checked | Improve ACL visibility |

## Category: User Experience

| Name | Description |
|------|-------------|
| Added a Number Prefix which already exists | Duplicate number records cause core functionality issues |
| List Inactive users from active group | List inactive users that still belongs to activate groups |
| HTTP connection records not excluded on clones | Orphaned records after clone |
| Avoid using alert() in client scripts | Use OOB modals instead of alert |
| Use "last run datetime" for JDBC data loads | Enable incremental JDBC loads |
| Use of setWorkflow(false) in business rules | Can cause unexpected behaviour |
| Make use of isLoading Check | Prevent unnecessary client script execution |
| Make sure columans are selected in list type reports | Improve list report user experience |
| Find Orphaned UI Policies | UI policies without actions or scripts |


# Additional resources

Please check these additional links for more information and details:

- [Platform Academy Foundation #5: Instance Scan Overview](https://community.servicenow.com/community?id=community_event&sys_id=f44eb0c0db82f410019ac22305961950)
- [Mark Roethof’s Blogs](https://community.servicenow.com/community?id=community_blog&sys_id=14e51965db2200d013b5fb24399619fb#is)
- [Live Coding Happy Hour – Instance Scan in Quebec (2021-03-12)](https://youtu.be/_cPlWnh1Z68)
- [Introduction to ServiceNow HealthScan and Instance Scan](https://nowlearning.service-now.com/lxp?id=overview&sys_id=e4c538231b0d6c505b2699f4bd4bcb6f&type=course)
- [K21 CCL1062 – Writing custom instance scan checks](https://nowlearning.servicenow.com/lxp/en/now-platform/introduction-to-servicenow-healthscan-and-instance-scan?id=learning_course_prev&course_id=fc3014c5db728150a87c2d3d569619d5)
- [Quebec Instance Scan](https://developer.servicenow.com/blog.do?p=/post/quebec-instancescan/)
