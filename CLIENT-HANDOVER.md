# Mfanageza Trading and Projects (Pty) Ltd
## Website project, Salesforce plan and client handover guide

**Purpose:** Explain the website and its proposed Salesforce back end in clear, everyday language.

**Project status:** Website draft prepared. Salesforce integration is a proposed next phase and is not confirmed as connected. Company information, final content, domain ownership and launch settings still require client approval.

---

## 1. Project overview

The project is to give Mfanageza Trading and Projects (Pty) Ltd a professional online presence and a better way to manage enquiries and business opportunities.

The solution has two parts:

1. **The website (front end):** The public-facing website. Visitors use it to understand the company, explore its areas of work and contact the team.
2. **Salesforce (back end):** A private business system for authorised staff. It can store enquiries, organise follow-ups and help the company see what needs attention.

The website and Salesforce have separate roles. The website is not a public view of the company's Salesforce records.

## 2. What the website is for

The website introduces the company to people and organisations that may want to ask about its services, discuss a project or explore working together.

The current draft allows visitors to:
- Learn who Mfanageza is.
- Read about the company's background and approach.
- Review the three areas currently described on the website.
- See the business contact locations supplied for the draft.
- Call the company or start a WhatsApp conversation.

The current draft does **not** include a working enquiry form, customer login, online payments, course registration or a live Salesforce connection. Those would be separately planned and tested features.

## 3. Website sections

| Section | What visitors will see |
| --- | --- |
| Home | A welcome message and a short explanation of the company. |
| About us | The company background, establishment date and founder information supplied for the draft. |
| Our areas of focus | Skills development, trading and business services, and project support. |
| Our approach | Listening, practical action and positive partnerships. |
| Our locations | The Johannesburg and Virginia addresses supplied for the draft. |
| Contact | The listed phone number and WhatsApp contact link. |

The design uses a modern blue visual style, clear headings, photographs and technology-inspired details. The layout is intended to work on desktop computers, tablets and mobile phones.

## 4. Company information to approve

The following information was supplied for the draft. The company should verify it before publication:

- **Company name:** Mfanageza Trading and Projects (Pty) Ltd.
- **Established:** September 2020.
- **Founder:** Bongani Mfana Ka Geza.
- **Phone / WhatsApp:** +27 81 426 0733.
- **Johannesburg address:** 53 Main Street Building, Johannesburg, Gauteng, 2001.
- **Virginia address:** 40 Tungsten Street, Saaiplaas, Virginia, Free State, 9430.
- **Areas of focus:** Skills development, trading and business services, and project support.

The company must confirm which addresses and contact details may be displayed publicly. The company should also approve the wording used to describe its services.

### Training and accreditation wording

The current website draft does not claim that Mfanageza is a university, TVET college or accredited training provider. It does not advertise a particular qualification, course, fee, intake date or accreditation.

Only publish training claims, course details, qualifications or accreditation after the company has confirmed them and supplied the correct supporting information.

### Photographs and brand material

The current design uses sample photographs from Unsplash. They are not represented as photographs of Mfanageza's staff, offices or clients. The company should provide its logo and approved photographs where available, and confirm that it has permission to use them.

## 5. How visitors will contact the company

The current draft includes:
- A phone link using the supplied company number.
- A WhatsApp link that opens a conversation with the supplied number.

These links should be tested on a mobile phone before launch. The company should confirm that the number is correct and that the person or team receiving messages is ready to respond.

A future website enquiry form could collect a visitor's name, contact details, enquiry category and message. The company should approve the exact fields and privacy wording before the form is built.

## 6. Proposed Salesforce back end

### What Salesforce will do

Salesforce is proposed as the company's private enquiry and relationship-management system. It can help authorised staff:
- Receive website enquiries in one place.
- See who made an enquiry and what they need.
- Assign an enquiry to a responsible staff member.
- Record follow-up actions and notes.
- Track progress from new enquiry to response or completion.
- Review reports showing enquiry volumes and follow-up status.

Salesforce is not automatically included in the current website draft. A Salesforce account, suitable licences, configuration and a tested connection will be required.

### Suggested first release: keep the data model simple

The recommended first release is to manage general business enquiries. Do not create a complicated system before the company has confirmed its real workflow.

| Salesforce record | Plain-language purpose |
| --- | --- |
| Lead | A new person or organisation that has contacted the company and has not yet become an established business relationship. |
| Account | A business or organisation the company deals with. |
| Contact | A person linked to a business or organisation. |
| Opportunity (optional) | A potential project, contract or piece of business that the company wants to track. |
| Task | A reminder to call, email or follow up with someone. |

Salesforce's standard records may be enough for the first version. Custom records should only be added when the company has a confirmed need.

### Possible enquiry categories

The website could let visitors choose a category such as:
- General enquiry.
- Skills development enquiry.
- Trading or business services.
- Project support or partnership.
- Other.

These categories are suggestions. The company must approve them and confirm which enquiries it actually wants to receive.

### Example of how the process could work

1. A visitor opens the Mfanageza website.
2. The visitor completes an approved enquiry form.
3. The website sends the enquiry securely to Salesforce.
4. Salesforce creates a new enquiry record.
5. An authorised staff member reviews it and assigns responsibility.
6. The staff member contacts the person and records the follow-up.
7. The enquiry is updated as it progresses.
8. Managers can review reports to see which enquiries need attention.

The process must be tested from the public website through to the Salesforce record before it is described as operational.

## 7. How the website and Salesforce can connect

The website is currently a static website hosted through GitHub Pages. GitHub Pages can display the website, but it does not provide a secure place to store Salesforce passwords or private connection keys.

There are two broad ways to connect the systems:

**Option A — Salesforce Web-to-Lead**
- A possible simple starting point for approved lead-capture forms.
- Form submissions can create Lead records in Salesforce.
- Salesforce configuration and spam protection are still needed.
- The company should check whether this approach meets its privacy, validation and workflow requirements.

**Option B — Secure integration service**
- The website sends form details to a secure server-side service.
- That service checks and validates the information, then sends it to Salesforce using an approved authentication method.
- It offers more control over validation, error handling and future workflows.
- It requires additional setup, hosting or service costs, testing and ongoing maintenance.

**Important security rule:** Never place Salesforce passwords, access tokens, client secrets or other private credentials in website JavaScript or public GitHub files. The best integration option should be selected after the company's needs, Salesforce licences and budget are confirmed.

## 8. Privacy and information protection

Enquiries may contain personal information. Before collecting information, the company should approve a clear privacy notice and decide what information is genuinely needed.

Recommended safeguards include:
- Collect only information needed to respond to the enquiry.
- Explain why information is collected and how it will be used.
- Identify who in the company may access enquiry records.
- Use individual staff accounts and appropriate access permissions.
- Avoid collecting identity numbers, health details or other sensitive information unless there is a clear, lawful and necessary reason.
- Decide how long records should be kept and how they will be securely disposed of.
- Protect the integration and prevent private credentials from being exposed.
- Agree who handles privacy requests, suspected data incidents and complaints.

The company should review its responsibilities under applicable South African privacy law, including POPIA, and obtain appropriate professional advice where needed. This document is a project guide, not legal advice or a compliance certification.

## 9. Suggested delivery phases

| Phase | Work | Completion evidence |
| --- | --- | --- |
| 1. Confirm the brief | Approve company details, services, contact information, photos and website content. | Written client approval. |
| 2. Finish the website | Complete the agreed pages, links, mobile layout and content checks. | Client-reviewed website draft. |
| 3. Domain and publishing | Register the chosen domain in the company's name, connect DNS and configure HTTPS. | Public domain opens securely. |
| 4. Salesforce setup | Confirm Salesforce account and licences; configure the agreed records, fields, users and permissions. | Staff can use the approved Salesforce process. |
| 5. Website connection | Build the approved form and secure connection method. | Test enquiry appears correctly in Salesforce. |
| 6. Testing and handover | Test mobile and desktop use, form validation, spam protection, permissions and follow-ups; train staff. | Test results and client sign-off. |

The phases can be adjusted after the client confirms the budget and priorities.

## 10. What the client needs to provide

### Website
1. Approved company description and service list.
2. Confirmed phone number and public business addresses.
3. Company logo and approved photographs, if available.
4. Approved social media links.
5. Any verified programme or training details the company wants to publish.
6. Approval of the final website wording and design.

### Salesforce
1. Confirmation that the company has a Salesforce organisation (account/environment).
2. The Salesforce administrator or authorised person who can approve access and configuration.
3. Confirmation of available Salesforce licences and any budget for extra services.
4. The staff members who will receive and manage enquiries.
5. The enquiry categories and steps staff follow after receiving an enquiry.
6. The information the company needs to collect, and its approved privacy notice and retention rules.
7. Approval of who can view, edit, assign and report on enquiry records.

Do not send passwords or private access tokens in email, chat or project documents.

## 11. Domain name and website address

The recommended domain to check first is:

**mfanageza.co.za**

It is shorter and easier to share than a long domain based on the full company name. Its availability and final registration price must be checked with a domain provider before purchase.

The domain should be registered in the company's name, using an account controlled by the company or its authorised representative. The company should retain control of renewals and account recovery.

The current GitHub Pages project address is:

https://kabelogopane.github.io/Mfanageza-Trading-and-Projects/

This is the project address, not proof that a custom domain has been registered or connected. The custom domain should only be announced after registration, DNS setup, HTTPS and live testing are complete.

## 12. Ownership, access and ongoing support

The company should retain ownership or administrative control of:
- Its domain registration account.
- Its Salesforce organisation and user accounts.
- Its company logo, photographs and approved content.
- Its business contact information and customer records.

The website project is stored in GitHub. The person maintaining it can update wording, images and website features when the company approves the changes.

The company should decide who is responsible for:
- Renewing the domain.
- Managing GitHub access and website updates.
- Managing Salesforce users and permissions.
- Reviewing new enquiries and following them up.
- Checking that the website, form and integration continue to work.

Any ongoing support arrangement, response times or additional development should be agreed separately.

## 13. Testing before launch

### Website checks
- [ ] Company details and service descriptions approved.
- [ ] Phone and WhatsApp links tested.
- [ ] Addresses approved for public display.
- [ ] Images and logo approved for use.
- [ ] Website checked on desktop, tablet and mobile.
- [ ] Navigation and page links tested.
- [ ] Domain registered and connected, if using a custom domain.
- [ ] HTTPS works and the public website opens correctly.

### Salesforce and form checks
- [ ] Salesforce account, licences and authorised administrator confirmed.
- [ ] Enquiry fields and categories approved.
- [ ] Privacy notice approved and visible beside the form.
- [ ] Test enquiry creates the correct Salesforce record.
- [ ] Required fields and invalid submissions are handled correctly.
- [ ] Spam protection and error handling tested.
- [ ] Staff permissions checked.
- [ ] Enquiry assignment and follow-up process tested.
- [ ] No private Salesforce credentials appear in public website files.
- [ ] Staff know how to review and manage enquiries.

## 14. Current project status

| Item | Status |
| --- | --- |
| Website structure and main content | Draft prepared |
| Modern responsive design | Included in current website files; final device testing required |
| Phone and WhatsApp links | Included; client confirmation and testing required |
| Company details and photos | Awaiting client verification/approval |
| Custom domain | Recommended name identified; registration not confirmed |
| GitHub Pages publishing | Must be checked before claiming the site is live |
| Salesforce configuration | Not yet confirmed or implemented |
| Website enquiry form | Not included in the current draft |
| Salesforce connection | Planned; not yet connected or tested |
| Final client sign-off | Pending |

## 15. Client approval

By approving the website, the company confirms that the public information, wording, images, contact details and service descriptions are suitable for publication.

Salesforce configuration and integration should have a separate approval covering the agreed features, access, privacy requirements, costs and testing.

**Company representative:** ______________________________

**Role:** _______________________________________________

**Signature:** ___________________________________________

**Date:** _______________________________________________

---

**Prepared for:** Mfanageza Trading and Projects (Pty) Ltd  
**Document:** Website Project, Salesforce Plan and Client Handover Guide  
**Important:** This document describes the website draft and a proposed Salesforce solution. It does not claim that the custom domain, website publishing, Salesforce setup or integration is already live. It is not a legal, accreditation or company-registration certificate.
