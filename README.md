# 🔐 Entra ID: Dynamic Groups & Access Management

## 📌 Project Overview
This lab is a hands-on demonstration of core group administration in Microsoft Entra ID. It covers creating Microsoft 365 collaborative groups, configuring dynamic security groups using query rules, delegating group ownership, and automating SaaS license allocation via group-based licensing.

## 🛠️ Skills & Technologies Demonstrated
* **Identity Platform:** Microsoft Entra ID, Microsoft 365 Admin Center
* **Group Lifecycle Management:** Creating M365 collaborative groups and standard security groups.
* **Dynamic Membership Rules:** Configuring automated security group membership using query parameters.
* **Access Management:** Delegating administrative ownership of directory objects.
* **Group-Based Licensing:** Automating SaaS application license allocation at the group tier.

## 📖 Business Scenario
"Wayne Enterprises" requires a structured grouping system to manage access for its specialized task forces. As the acting Identity Administrator, the objective is to create an M365 collaborative group for internal operations, build a dynamic security group to automatically capture and isolate all off-world guest consultants, delegate group ownership to a team lead, and apply group-based licensing to streamline resource allocation.

---

## 🚀 Step-by-Step Implementation

### Phase 1: Create the "Project Watchtower" Group
Established an M365 group with assigned membership to facilitate team collaboration and shared resource access.

1. Navigated to the [Microsoft Entra admin center](https://entra.microsoft.com) and authenticated using Tenant administrator credentials.
2. From the left navigation menu, selected **Groups** > **All groups**.
3. Selected **New group** at the top.
4. Configured the following group details:
   * **Group type:** Microsoft 365
   * **Group name:** Project Watchtower
   * **Membership type:** Assigned
5. Under the "Members" section at the bottom, clicked the blue text that says **No member selected**.
6. Searched for **Clark Kent**, and selected his name to move it to the "Selected items" area.

 <p>
  <img src="https://imgur.com/3LBL9G5.png" height="80%" width="80%" />
</p>
8. Clicked the **Select** button, then clicked **Create** to deploy the group.

### Phase 2: Create the Dynamic "Off-World Guests" Group
Implemented automated group membership scaling by creating a security group driven by a dynamic query.

1. Returned to the **All groups** page and selected **New group**.
2. Configured the following details:
   * **Group type:** Security
   * **Group name:** Off-World Guests
   * **Membership type:** Dynamic User
3. Under the "Dynamic user members" section, clicked **Add dynamic query**.
4. Configured the rule syntax to automatically target external identities:
   * **Property:** userType
   * **Operator:** Equals
   * **Value:** Guest
   <p>
  <img src="https://imgur.com/RM5qb2E.png" height="80%" width="80%" />
</p>
5. Clicked **Save** at the top, and then clicked **Create** at the bottom.
6. *Note: Allowed 5 minutes for the dynamic group to populate.* Navigated to the **Members** tab of the new "Off-World Guests" group to validate that the query successfully pulled in the guest users (e.g., Thor Odinson).
   <p>
   <img src="https://imgur.com/THnFmbi.png" height="80%" width="80%"/>
   </p>

### Phase 3: Manually Add a User to a Group
Demonstrated post-creation directory management by appending new identities to an established group.

1. Navigated to the **All groups** list and selected the **Project Watchtower** group.
2. Selected **Members** from the left-hand menu.
3. Clicked **+ Add members** from the top command bar.
4. Searched for **Diana Prince**, and checked the box next to her name.
   <p>
   <img src="Ihttps://imgur.com/Om96L2b.png" height="80%" width="80%"/>
   </p>
5. Clicked **Select** to successfully add her to the group.

### Phase 4: Delegate Group Ownership
Adhered to decentralized management practices by delegating administrative control of the group.

1. From the **Project Watchtower** menu, selected **Owners** on the left side menu.
2. Clicked **+ Add owners** at the top.
3. Searched for **Clark Kent**, and checked the box next to his name.
   <p>
   <img src="https://imgur.com/Hz5XA8L.png" height="80%" width="80%"/>
   </p>
4. Clicked **Select** to assign him administrative control over the group.

### Phase 5: Assign Licenses to the Group
Applied enterprise licenses at the group tier to automate SaaS provisioning.

1. Opened a new browser tab and navigated to the [Microsoft 365 admin center](https://admin.microsoft.com).
2. Expanded the **Billing** menu and selected **Licenses**.
3. Selected an available operational license (e.g., Office 365 E5 or Power Automate Free).
4. Selected the **Groups** tab near the top of the page.
5. Clicked **+ Assign licenses**.
6. Searched for **Project Watchtower** and selected it in the dropdown.
   <p>
   <img src="https://imgur.com/i3zUorU.png" height="80%" width="80%"/>
   </p>
7. Clicked the **Assign** button at the bottom.
8. Verified the successful deployment via the confirmation banner.
   <p>
   <img src="https://imgur.com/5azPY4t.png" height="80%" width="80%"/>
   </p>

---
*Disclaimer: This repository is for educational and portfolio demonstration purposes. No actual Kryptonians or Asgardians were harmed during the making of this lab.*
