# Rohan's notes: follow-up meeting with Friendly Staffing

Captured 2026-11-03. Rohan's notes from the latest meeting with the Friendly Staffing team, as shared. Part 1 (worker status, shortlisting, approvals, replacements, orders) and part 2 (pay and invoicing).

---

Okay, so employee codes are created only when employees are assigned their first job, not before that. Before that, they are called inactive employees, and as soon as they are allotted or assigned their first job, they are marked as active and that's when their employee code is generated. Until then, if you want to identify employees, maybe we can have temporary employee codes.

The logic for shortlisting as well as prioritizing candidates on a new job remains to be dynamic, and we should be giving them an ability to make changes to that prioritization order.

There are two kinds of employees: there are contractual workers and direct deduction. The way payment happens to direct deduction versus contractor is different.Okay.

In most and general cases, there is no employer approval required before sending finalized candidates or employees to the job. It's friendly-staffing's responsibility, as well as the whole job, that the right kind of candidates and the right kind of employees with the right qualification and the right experience are available to the employers based on their requirements.

There are some employers who have different approval processes as well as trials, in which case we can create a new workflow for approval. The approval might happen over an email. The trials may also happen physically or in some other manner, but that needs to be scoped later. For now, we need to make sure that there is a separate workflow where approvals can be processed.

Replacement/no-show workflow for worker side as well as for employer side needs to be arranged. The friendly-staffing team will have some actions to perform if the worker does not show up for a new replacement to be arranged.

An employer's request: we should be able to add, edit, or delete that request because often employers change their requirements as they go closer to the actual job date. We need to make sure that such flexibility is available.

---

## Part 2: pay and invoicing (shared 2026-11-03)

Okay, so the current process friendly-staffing follows to process invoices, as well as payments to or wages to employees, is as follows:

There's a timekeeper at every job location which basically manages punch-ins and punch-outs on a daily basis. At the end of the week, we get a timesheet PDF that I've attached in the inbox with the week's attendance as well as the number of hours worked that basically gets converted into a PDF.

Its data goes into an Excel sheet, which is a database of employees that friendly-staffing has, and that database basically tells us what's the going rate for the job that an employee is on and the payment method he prefers.

Okay, so there's a PDF sheet that is basically a timesheet available in our inbox that goes into an Excel sheet for payments. That Excel sheet is basically a database of employees under the employer names and the rates at which they are contractors or the rates at which they are employed.

That sheet will give us the gross pay. Once gross pay is available, typically there are two ways employees can be paid under two methods:

1. Payment method A, which is basically direct-deduction. Employees are considered full-time employees and government deductions are applicable.
2. Payment method B, which is subcontractors. Employees are employed as subcontractors, in which case there are no deductions applicable.

Employees are often given an option as to which payment method they want to be compensated via. Employees can select one or the other, or both payment method A and payment method B.

After processing them through that, we get a final number after deductions, which can be used to put in our accounts as well as be put in the bank portal from which the payments can be processed.

Now, the rates at which these people are employed—Friendly Staffing's margin is yet to be decided, and how the working of that happens is yet to be understood completely. But basically, once payment type A and payment type B's output is received, we create a stub.

A stub is created on QuickBooks. On QuickBooks, under employer, you enter an employee's name. You put in the number of hours he's worked, whether it's under payment type A or payment type B within QuickBooks itself, and you put the final pay that is applicable under that payment type for that employee, and then you record that transaction.

At the same time, you export—typically you would want to export an XML file rather than a QuickBooks summary—which you can then import into the bank portal from which the payment processing can happen.

This way, we have made sure that the employees' correct gross pay is recorded and correct deductions are applied depending on the payment method they have chosen, payment method A or payment method B. You record the right transactions on QuickBooks, and based on all of this information, you make sure that the bank also gets the right figures for the right employees.

Now, the first Excel sheet which is created after the timesheets is also used to create invoices for the client. Since there are very few clients, it's a manual recording of invoices on QuickBooks; an invoice is generated and then sent to the employer who in turn pays that invoice.

Both of these processes happen on a weekly basis. There's an element of regular pay as well as overtime pay, for which the rates differ, but otherwise, all in all, it remains the same.

The timesheet PDF referred to is `00-inbox/23083148_260817.pdf` (Molinaro's, week of 2026-08-10; kept out of git).

## Part 3: Rohan's answers on payroll, and the phase change (shared 2026-11-03)

1. Okay, so method A deductions are calculated in Excel today and then verified in QuickBooks later.
2. The pay is split when a worker chooses both methods by hours. Regular hours get split and so do overtime hours, and it can't change week to week. But we do need to offer an ability to change later
3. I don't think that should matter right now. Let's just keep it as a task or module. I don't have details on this right now.
4. No, we don't have the details on it yet, but we'll probably account for any variability and we'll account for slightly more hours.
5. Yes, it can be.

- No workers are paid outside the bank file.Workers can be paid via payment method A or payment method B, with deductions or without deductions, but all payments happen through the bank. The way the rates at which we are calculating gross pay for workers, and then creating stubs, gross deducting the deductions etc., is all something that happens at the rate which is called pay rate. The bill rate is completely separate and agreed between both parties.So the way we are deriving bill rate is slightly more unknown right now. Currently every site has a timekeeper, but eventually when we manage timekeeping of our own, it has to be a separate module. It has to be managed inside flow as well, but that can be agreed later whether you want to keep timekeeping as a separate module and to be done later or to be included in the scope right now. But right now we're keeping it as part of the scope.

- Currently friendly-staffing pays around 8,000 US Canadian dollars to QuickBooks for payroll management as well as accounts. If we remove payroll management from QuickBooks completely, then that cost reduces dramatically.

So Tejas, in our last call, recommended that we move the finalizing of payroll as well as creating stubs in Phlo in our new software, after which the final amounts can then be pushed to the accounts, which basically includes recording of the transaction. The timekeeping, as well as the payroll management and XML that we are thinking for phase two, we need to include in phase one (can you confirm this?)

Information requested from Friendly Staffing (as drafted by Rohan):

- Payroll Excel samples of the pay stops
- The bank XML
- A client invoice
- How payment method A and payment method B are calculated
- How net pay is calculated from CrossPay

## Part 4: Rohan's answers on scope and sizing (shared 2026-11-03)

1. The actual calculation can happen in Phlo, the actual payment that happens to the government and from the government that has to be outsided. Actually, 4 of these things can be added as well. I don't mind it in scope.
2. WhatsApp Business plus email with SMS sounds like a right messaging channels
3. In most cases, employer approval is not required. In cases where employer approval is required or a trial is required, we are going to build a separate workflow, so we'll account for that and standardize and account for that.
4. One order for the whole business, with overriding possible with different clients or different roles.
5. For this question, I need to understand whether the timesheets are approved and signed by the employers first and after that it reaches friendly-staffing or not.
6. Added each week. This is a question that I need to ask Tejas. So, why don't we create a small message for this as well and I'll message him separately.
7. friendly-staffing staff 4 to 5. We're not gonna use tablets. Probably manage in phones, so timekeeper can manage it on her phone. Signatures can happen by the employees via their phones as well. So the whole attendance marking, as well as breaks punching in and out, marking present, and marking absent, all of these things are yet to be figured out in terms of the workflow.
8. 300 to 400.
9. QuickBooks year-to-date history as well.
10. Yeah, English only.
11. The target goal I would be by January 15th.

Commercial answers (12 and 13) are kept in `00-inbox/internal-commercials-2026-11-03.md`, which is not committed because this repository is public.
