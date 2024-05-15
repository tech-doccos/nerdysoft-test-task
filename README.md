# User Stories: Currency Management

## Goal&nbsp; <img src="resources/images/goal.png" style="width: 30px; height: 30px;margin-top: 20px;">

Enable users to manage currencies effectively within the system.

## Glossary&nbsp; <img src="resources/images/glossary.png" style="width: 30px; height: 30px;margin-top: 20px;">

* **Acceptance criteria:** Specific conditions that must be met for a user story to be considered complete, outlining the expected behavior or functionality.

* **Artifact:** A tangible item produced or managed during the software development process.

* **Legal tender:**  Currency recognized by law as valid for transactions within a particular jurisdiction, typically issued and regulated by a government or central authority. In simple terms, it is the national currency of a particular country.

* **Permission:** Authorization or access rights granted to users, determining what actions they are allowed to perform within the system.

* **Purpose:** The reason behind a user story or feature, explaining the intended outcome or benefit for the user or business.

* **Reference Currency:**  A designated currency within a system used as a standard for comparison or as a basis for currency-related operations.

* **Role:**  The specific user or stakeholder for whom the software is being developed, defining their identity and responsibilities within the system.

* **User Story:**  A brief description of a feature or functionality from the perspective of an end user, stating what they want to accomplish and why it is important.

## User Story: View List of Currencies &nbsp;<img src="resources/images/view-list.png" style="width: 30px; height: 30px;margin-top: 20px;">

<table>
<tr>
    <td><strong>Role:</strong></td>
    <td>User.</td>
</tr>
<tr>
    <td><strong>Goal:</strong></td>
    <td>Ability to view a list of currencies.</td>
</tr>
  <tr>
    <td><strong>Purpose:</strong></td>
    <td>Ability to get actual information about the existing currencies and currencies used in the bank.</td>
</tr>
    <tr>
    <td><strong>Artifact:</strong></td>
    <td>Currencies.</td>
</tr>
</table>

### Acceptance Criteria:

**1.** If you have permission to view currencies (`VIEW_CURRENCIES`, `MANAGE_CURRENCIES`, `SET_REF_CURRENCY`), there is an item for "Currency Management" in the system menu.

**2.** Having the permissions listed above, you click on the "Currency Management" item, which shows you a list of currencies.


## User Story: View Currency Details &nbsp;<img src="resources/images/view-details.png" style="width: 30px; height: 30px;margin-top: 20px;">

<table>
<tr>
    <td><strong>Role:</strong></td>
    <td>Administrator.</td>
</tr>
<tr>
    <td><strong>Goal:</strong></td>
    <td>Ability to view currency details.</td>
</tr>
  <tr>
    <td><strong>Purpose:</strong></td>
    <td>Ability to get actual information about the currency and its usage in the bank.</td>
</tr>
    <tr>
    <td><strong>Artifact:</strong></td>
    <td>Currencies.</td>
</tr>
</table>

### Acceptance Criteria:

**1.** When you click on a selected currency from the list, it shows you the details of that currency.

**2.** If you have permission to manage currencies (`MANAGE_CURRENCIES`, `SET_REF_CURRENCY`), the button to edit the currency is available.

**3.** When you close the currency details screen, it should take you back to the currency list.


## User Story: Add Currency &nbsp;<img src="resources/images/plus.png" style="width: 30px; height: 30px;margin-top: 20px;">

<table>
<tr>
    <td><strong>Role:</strong></td>
    <td>Administrator.</td>
</tr>
<tr>
    <td><strong>Goal:</strong></td>
    <td>Ability to add currency.</td>
</tr>
  <tr>
    <td><strong>Purpose:</strong></td>
    <td>To make it available in the system.</td>
</tr>
    <tr>
    <td><strong>Artifact:</strong></td>
    <td>Currencies.</td>
</tr>
</table>


### Acceptance Criteria:

**1.** Being able to see the currency list, you can initiate adding currency, if you have `MANAGE_CURRENCIES`, `SET_REF_CURRENCY` permission.

**2.** When adding a currency, you can enable cash operations if needed (field shows `Non-cash operations = True`).

**3.** When adding a currency, you can enable legal tender if needed (field shows `Cash operations = True`).

**4.** To set the new currency as a reference currency, the following conditions must be true: 

* Field `Legal tender = True`.

* There is no currency where the field `Reference currency = True`.

* You have permission `SET_REF_CURRENCY`.
  
**5.** After entering currency details, the system should validate them. If everything is correct, it saves the currency and shows you the updated currency list. The system will display a relevant message for a given validation.

**6.** If you try to cancel adding currency with unsaved changes, the system will prompt you to confirm. It discards the changes if confirmed and returns you to the currency list.

## User Story: Edit Currency &nbsp; &nbsp;<img src="resources/images/edit.png" style="width: 30px; height: 30px;margin-top: 20px;">

<table>
<tr>
    <td><strong>Role:</strong></td>
    <td>Administrator.</td>
</tr>
<tr>
    <td><strong>Goal:</strong></td>
    <td>Ability to edit currency.</td>
</tr>
  <tr>
    <td><strong>Purpose:</strong></td>
    <td>Ability to adjust currency details or its usage in the bank.</td>
</tr>
    <tr>
    <td><strong>Artifact:</strong></td>
    <td>Currencies.</td>
</tr>
</table>

### Acceptance Criteria:

**1.** From the currency list, you should be able to select and edit currency, if you have `MANAGE_CURRENCIES`, `SET_REF_CURRENCY` permission.

**2.** If you have any of the permissions listed above, you should be able to initiate editing from the currency details.

**3.** When editing currency, you can enable cash operations if needed (field shows `Non-cash operations = True`).

**4.** When editing currency, I should be able to enable legal tender if needed (the field shows `Cash operations = True`).

**5.** To set a new currency as the reference currency, the following conditions must be true: 

* Field `Legal tender = True`.

* There is no currency where the field `Reference currency = True`.

* You have permission `SET_REF_CURRENCY`.

**6.** After editing currency details, the system should validate them. If everything is correct, it should save the changes and show me the updated currency list. The system will display a relevant message for a given validation. 

**7.** If you try to cancel editing currency with unsaved changes, the system should prompt you to confirm. If confirmed, it should discard the changes and return you to the currency list.

**8.** If a currency is set as the reference currency, you will not be able to edit the following fields: 

* `Reference currency`.

* `Legal tender`.

* `Cash operations`. 

* `Non-cash operations`.


