# Mfanageza Trading and Projects
## Website delivery and Mfanageza CRM integration plan

**Purpose:** This guide explains the website, the business process it should support, and how it can connect to the existing Mfanageza CRM Salesforce project. It is written for the client and the people implementing the project.

**Document status:** Project plan and delivery guide. The website is a draft. The Salesforce CRM has a working foundation, but the public website connection has not been built or tested. Do not describe the integration as live until an end-to-end test has passed.

---

## 1. The project in simple terms

Mfanageza will have one public website and one private business system.

- **Website:** The public front door. Visitors learn about the company, explore its services and find the right way to contact or apply.
- **Mfanageza CRM (Salesforce):** The private back office. Approved staff manage candidate details, applications, programmes, documents, checks, follow-ups and reports.
- **Connection:** An approved form on the website sends information to Salesforce through a controlled Salesforce service. The website must never contain Salesforce passwords or private access keys.

The website and CRM have different jobs. A website visitor must not be able to browse private candidate or company records.

## 2. Website project details

### Business identity

- **Business name:** Mfanageza Trading and Projects (Pty) Ltd.
- **Country:** South Africa.
- **Public message used in the draft:** “Growing people. Creating possibilities.”
- **Supporting theme:** “People. Potential. Progress.”
- **Established:** September 2020 (company to confirm).
- **Founder:** Bongani Mfana Ka Geza (company to confirm).

### Design direction

The website uses a modern blue visual identity with orange and yellow highlights, strong headings, photography, simple navigation and technology-inspired details. It is designed to be clear on desktop, tablet and mobile screens.

The design is intended to feel professional, modern and forward-looking. It must not suggest that Mfanageza is an accredited college, university or training provider unless the company supplies evidence and approves that wording.

### Current website sections

| Section | Purpose |
| --- | --- |
| Home | Introduces Mfanageza and its people-first message. |
| About us | Explains the company background, founding date and founder details supplied for the draft. |
| Our services | Describes skills development, trading and business services, and project support. |
| Our approach | Explains listening, practical action and positive partnerships. |
| Locations | Shows the Johannesburg and Virginia addresses supplied for the draft. |
| Contact | Provides the telephone and WhatsApp contact links. |

### Current visitor actions

At present, visitors can read the company information, navigate between sections, call the listed number or open a WhatsApp conversation.

The current website does **not** yet provide:
- A working website enquiry form connected to Salesforce.
- Candidate registration or programme applications.
- A candidate login or private portal.
- Document upload or compliance tracking.
- Online payments.
- A live CRM connection.

These are planned additions, not completed features.

### Website project files

- `index.html` — the website content and page sections.
- `styles.css` — colours, fonts, layout, responsive design and visual effects.
- `script.js` — mobile navigation, current-year footer and scroll reveal effects.
- `README.md` — project overview and basic publishing notes.
- `CLIENT-HANDOVER.md` — plain-language website handover guide.
- `WEBSITE-AND-SALESFORCE-INTEGRATION.md` — this full delivery and integration plan.

### Current website address

The GitHub Pages address planned for the draft is:

https://kabelogopane.github.io/Mfanageza-Trading-and-Projects/

The preferred custom domain to check is **mfanageza.co.za**. It is not confirmed as registered or connected. The company should own the domain registration account. After registration, the DNS records and GitHub Pages custom-domain settings must be configured and tested before the custom address is advertised.

## 3. Company information that needs approval

The following details were supplied for the draft. The company must verify them before public launch:

- Company name and legal spelling.
- Founding date and founder information.
- Telephone and WhatsApp number: +27 81 426 0733.
- Johannesburg address: 53 Main Street Building, Johannesburg, Gauteng, 2001.
- Virginia address: 40 Tungsten Street, Saaiplaas, Virginia, Free State, 9430.
- Services and areas of focus.
- Approved logo, photographs and social media links.

The draft currently uses sample Unsplash photographs. They are not photographs of Mfanageza staff, offices, learners or clients. Replace them with approved company images when available, or confirm that the sample images may remain.

The company must confirm any course names, programme availability, fees, dates, qualifications, accreditation or training claims before they are published. The current wording deliberately avoids claiming that Mfanageza is a university, TVET college or accredited training provider.

## 4. The existing Mfanageza CRM project

The Salesforce project is intended to manage the candidate and programme journey. It is not a new CRM that needs to be started from zero.

### Existing CRM foundation

The CRM work recorded so far includes:
- Salesforce Developer Edition environment used for development (previously identified as `dyict-dev-ed`; confirm the active org before integration).
- Contacts used as Candidate records, with the Candidate label.
- Candidate Application custom object.
- Programme custom object.
- Compliance Document custom object.
- Relationships between candidates, applications, programmes and compliance documents.
- A Mfanageza CRM Lightning app and navigation.
- Three validation rules recorded as completed.
- A rejection-email automation recorded as built.
- A Candidate Application Flow was recorded as in progress.
- Reports, dashboards, data import, full end-to-end testing and final evidence were still outstanding in the last recorded project update.

Check the live Salesforce org before relying on this list. The actual configuration may have changed since that update.

### Main CRM records

| Salesforce record | What it represents |
| --- | --- |
| Contact (labelled Candidate) | A person who is applying or has applied. |
| Candidate Application | One application submitted by a candidate for a programme. A candidate may have more than one application over time. |
| Programme | A programme or opportunity that candidates can apply for. |
| Compliance Document | A document linked to an application and reviewed by authorised staff. |

### Candidate information

The planned candidate information includes candidate name, email, phone, South African ID number, province and employment status. Confirm the final field list and required fields in Salesforce.

### Candidate Application information

The recorded application fields include:
- Application Number (auto-number).
- Candidate relationship.
- Application Date.
- Application Status.
- Programme relationship.
- Programme Type.
- Start Date.
- Employment Status.
- Province.
- SETA.
- SETA Registration Status.

Confirm the exact API names, field types, required settings and picklist values in the active Salesforce org before building the website connection.

### Programme information

The planned Programme fields include Programme Name, Programme Type, SETA, NQF Level, Capacity, Start Date, End Date and Status.

### Compliance Document information

The planned document fields include Document Name, Candidate Application, Document Type, Verification Status, Upload Date, Verification Date and Rejection Reason. The earlier design also included a Verified By staff-user relationship.

Example document categories discussed for the CRM include an SA ID copy, CV, Matric certificate and proof of residence. These documents contain personal information and must not be exposed through public website pages.

### Example CRM progress flow

The intended compliance process is:

**Submitted → Under Review → Approved or Rejected**

The intended application process also uses the selected Programme and SETA registration information to guide application status. The exact automation rules must be checked and tested in the live org before launch.

## 5. How the website and CRM should work together

The website should direct each visitor to the correct journey. There are two different types of interaction:

### Journey A: General business enquiry

For a person or organisation asking about services, trading, project support or partnerships:

1. Visitor opens the Mfanageza website.
2. Visitor chooses “General enquiry” or a relevant service category.
3. Visitor completes a short enquiry form.
4. Salesforce receives the enquiry as a Lead (or another record type approved by the company).
5. An authorised staff member reviews and assigns the enquiry.
6. Staff contact the person and record the next action.
7. The enquiry is updated until it is closed or converted into an established business relationship.

This business enquiry journey should not create a Candidate Application unless the person is actually applying for a programme.

### Journey B: Candidate application

For a person interested in applying for a Mfanageza programme:

1. Visitor selects “Apply” or “Programme enquiry” on the website.
2. The website opens the approved Salesforce application experience.
3. The applicant completes the approved registration/application steps.
4. Salesforce checks for an existing candidate where possible to reduce duplicate records.
5. Salesforce creates or updates the Candidate (Contact) record and creates a Candidate Application linked to the selected Programme.
6. The applicant receives a clear confirmation or reference number if the flow has been configured to provide one.
7. Authorised staff review the application in Mfanageza CRM.
8. Staff update application and SETA registration statuses and carry out the required checks.
9. Compliance documents are handled through a suitably protected process.
10. Staff use Salesforce reports and dashboards to monitor workload and progress.

The company must approve the applicant journey, programme choices, required information, confirmation wording and staff responsibilities before it is built.

## 6. Recommended technical connection

### Recommended starting design: Salesforce Experience Cloud with a Screen Flow

The current public website is a static website hosted on GitHub Pages. A static website should not connect directly to Salesforce using a password, access token or private client secret in browser code.

A practical first version is:

1. Keep the existing Mfanageza website on GitHub Pages.
2. Create and configure a suitable Salesforce Experience Cloud site in the Salesforce org, if the org edition, features and licensing support the required setup.
3. Build a Salesforce Screen Flow for the approved public enquiry or application steps.
4. Add the Flow to a carefully configured public Experience Cloud page.
5. Put a clear button or link on the GitHub Pages website that opens that Salesforce page.
6. Configure only the minimum guest access needed for that specific process.
7. Test the full journey from a signed-out browser through to the correct Salesforce record.

Salesforce documents that a public Experience Cloud site can host a Screen Flow for collecting information, including registration and lead-capture forms. Guest access, Flow access and object permissions must be deliberately configured. See the official guidance:
- https://help.salesforce.com/s/articleView?id=platform.flow_distribute_external_experience_guest_user.htm&language=en_US&type=5
- https://developer.salesforce.com/docs/platform/communities-dev/guide/communities-dev-security-authenticated-and-guest-users.html

**Important:** This is a recommended design, not a statement that Experience Cloud is already enabled or included in the current Salesforce Developer Edition. Check the org's available features, external-user licensing, limits and current Salesforce terms before committing to this approach.

### Later option: a fully branded candidate portal

A later phase can provide a more complete candidate experience, such as:
- Candidate sign-in and account recovery.
- A private view of the candidate's own applications.
- Application status and reference number.
- Secure document submission.
- Requests for missing information.
- Notifications when application status changes.

This should use an authenticated and properly permissioned Salesforce Experience Cloud design or another approved secure application. It should not be implemented as a public page that exposes CRM records.

### When a separate integration service is needed

If the company later requires the website to communicate with Salesforce without sending visitors to an Experience Cloud page, use a secure server-side integration service. That service must protect credentials, validate incoming data, handle errors and use an approved Salesforce OAuth method. It requires additional hosting, development, security review and maintenance.

Do not put Salesforce passwords, OAuth client secrets, access tokens or refresh tokens in:
- `index.html`
- `styles.css`
- `script.js`
- Public GitHub files
- Browser-visible configuration

Salesforce's current OAuth guidance recommends External Client Apps for new integrations; Salesforce notes that creation of new Connected Apps is restricted as of Spring '26. Choose the current supported authentication method when the integration is actually designed:
- https://help.salesforce.com/s/articleView?id=sf.external_client_apps_oauth_flow_config.htm&language=en_US&type=5
- https://help.salesforce.com/s/articleView?id=xcloud.remoteaccess_oauth_web_server_flow_ca.htm&language=en_US&type=5

## 7. Security and personal information

Candidate applications may contain personal information, including identity details and supporting documents. The company should approve the information it collects, explain why it is needed and restrict access.

Minimum safeguards:
- Collect only information needed for the stated purpose.
- Show an approved privacy notice before a person submits information.
- Do not collect a South African ID number or sensitive supporting documents in a basic public enquiry form.
- Do not make candidate records or documents publicly readable.
- Do not give public visitors access to broad Candidate, Candidate Application or Compliance Document permissions.
- Use least-privilege access for guest users, staff and external users.
- Restrict document access to authorised staff and the correct candidate.
- Use individual staff accounts; do not share administrator logins.
- Decide how long records are retained and how requests or incidents are handled.
- Test access using a signed-out browser and different user roles.
- Keep private integration credentials out of GitHub and browser code.

The company should review its responsibilities under South Africa's Protection of Personal Information Act (POPIA) and obtain appropriate professional advice. This project guide is not legal advice or a compliance certificate.

## 8. Delivery plan and order of work

| Stage | Work to complete | Evidence before moving on |
| --- | --- | --- |
| 1. Client approval | Confirm company details, services, contact information, photos, domain and wording. | Written approval from the company. |
| 2. Website completion | Review all sections, mobile layout, links, accessibility and final images. | Website review checklist signed off. |
| 3. Publish and domain | Confirm GitHub Pages publishing, register the company domain, configure DNS and HTTPS. | Public website and custom domain tested. |
| 4. CRM review | Inspect the active Salesforce org, existing objects, fields, flows, validation rules, permissions and licences. | Confirmed CRM configuration and gap list. |
| 5. Candidate process design | Agree application stages, programme choices, required fields, duplicate handling, confirmation and staff workflow. | Approved process map and field list. |
| 6. Public form prototype | Build the agreed Screen Flow and Experience Cloud page if supported by the org. | Public test submission creates the intended record. |
| 7. Secure document process | Design authenticated document submission and staff verification permissions. | Access and privacy tests passed. |
| 8. End-to-end testing | Test general enquiries, candidate applications, duplicates, validation, errors, notifications and reporting. | Test evidence and resolved defects. |
| 9. Staff handover | Train authorised staff and provide a simple operating guide. | Staff acceptance and handover sign-off. |

Do not start by adding every possible feature. First prove one complete, low-risk journey: a test visitor submits an approved enquiry or application and the correct record appears in Salesforce with the right access controls.

## 9. Testing checklist

### Website checks
- [ ] Company has approved all public content.
- [ ] Phone and WhatsApp links work.
- [ ] Navigation works on desktop and mobile.
- [ ] Images are approved and load correctly.
- [ ] No placeholder or misleading course/accreditation claims remain.
- [ ] Website opens securely over HTTPS.
- [ ] Custom domain is registered to and controlled by the company.

### Salesforce checks
- [ ] Correct Salesforce org and environment confirmed.
- [ ] Existing Candidate, Candidate Application, Programme and Compliance Document records reviewed.
- [ ] Required fields and picklist values confirmed.
- [ ] Candidate duplicate handling tested.
- [ ] Application is linked to the correct Candidate and Programme.
- [ ] Status automation behaves as approved.
- [ ] Only authorised staff can see candidate details and documents.
- [ ] Guest access is limited to the exact public process.
- [ ] Errors are handled without losing or exposing personal information.
- [ ] Reports show accurate test data.

### End-to-end checks
- [ ] A signed-out visitor can open the public application/enquiry page.
- [ ] A valid test submission reaches the correct Salesforce record.
- [ ] Invalid or incomplete submissions are handled clearly.
- [ ] Duplicate submissions are handled according to the approved rules.
- [ ] The visitor receives the correct confirmation.
- [ ] Staff can find, assign and process the record.
- [ ] No private CRM information is visible to the public.
- [ ] The company has approved the final result.

## 10. What the company needs to provide

### Website
1. Final approved company description and service list.
2. Confirmation of phone number and public addresses.
3. Company logo and approved photographs.
4. Approved social media links.
5. Verified programme/training information, if it should be published.
6. Approval of the design and final wording.
7. Decision and budget for the custom domain.

### CRM and integration
1. Access to the correct Salesforce administrator or authorised project owner (never share passwords in project documents).
2. Confirmation of the active Salesforce org and edition.
3. Confirmation of available Experience Cloud features, licences and limits.
4. Final candidate application process and programme list.
5. Required candidate information and which fields are genuinely necessary.
6. General business enquiry categories and who handles them.
7. Staff roles and record-access requirements.
8. Approved privacy notice, retention policy and process for handling privacy requests.
9. Confirmation of who will own ongoing support and maintenance.

## 11. Client handover: what is delivered and what is not

### Prepared in the website project
- A responsive public website draft.
- Company introduction and service sections based on supplied information.
- Phone and WhatsApp contact links.
- Website project files stored in the GitHub repository.
- Plain-language handover and integration planning documents.

### Existing CRM work to verify in Salesforce
- Candidate/Contact structure.
- Candidate Application, Programme and Compliance Document objects.
- Related records and CRM navigation.
- Validation and automation work previously recorded.
- Remaining Flow, reporting, testing and documentation tasks.

### Not yet confirmed as delivered
- A registered and connected custom domain.
- Final client-approved website content and images.
- A production-ready Salesforce CRM.
- A live public application form.
- A working website-to-Salesforce connection.
- Candidate login, secure document upload or candidate self-service portal.
- Production security, privacy review and staff training.

The project is complete only when the client approves the website, the agreed Salesforce process works from end to end, security tests pass and the handover is accepted.

---

## 12. Official Salesforce references

- Public Screen Flow on an Experience Cloud site: https://help.salesforce.com/s/articleView?id=platform.flow_distribute_external_experience_guest_user.htm&language=en_US&type=5
- Guest and authenticated user security: https://developer.salesforce.com/docs/platform/communities-dev/guide/communities-dev-security-authenticated-and-guest-users.html
- Experience Cloud self-registration and login: https://help.salesforce.com/s/articleView?id=experience.networks_customize_login.htm&language=en_US
- OAuth setup for External Client Apps: https://help.salesforce.com/s/articleView?id=sf.external_client_apps_oauth_flow_config.htm&language=en_US&type=5

**Final reminder:** The website is the public entrance. Salesforce is the protected system behind it. Keep those responsibilities separate, collect only approved information and never expose private Salesforce credentials or candidate records on the public website.
