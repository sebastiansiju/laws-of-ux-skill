# Example: Signup form review

This is a sample of what the `ux-laws-review` skill produces. The form below is a typical made-up SaaS signup page, used for illustration.

## Prompt

> Review this signup form against the Laws of UX.
>
> One long page with: First name, Last name, Email, Confirm email, Password, Confirm password, Phone (must be in format +44 7XXX XXXXXX), Company, Job title, Company size (dropdown, 12 options), Country (dropdown, 195 options), "How did you hear about us?" (dropdown, 14 options), two checkboxes for marketing emails, a small grey "Create account" button at the bottom left, and a "Cancel" button of the same size and colour next to it. After submitting there's a 3-second blank screen, then the user lands on an empty dashboard.

## Output

### Issues by law

**Hick's Law**: 13 fields and three long dropdowns on one page means a lot of decisions before any value.
→ Ask only for email and password up front. Collect company, job title, company size and referral source later, during onboarding or never.

**Miller's Law**: The fields form one long undifferentiated list.
→ If you must keep extra fields, group them into "You" and "Your company" with clear headings, or split them into two short steps.

**Postel's Law**: The phone field rejects anything not in exactly `+44 7XXX XXXXXX`.
→ Accept spaces, dashes, brackets and numbers without a country code, then normalise on the server. Better still, make phone optional.

**Tesler's Law**: "Confirm email" and "Confirm password" push work onto the user.
→ Drop them. Add a show/hide toggle on the password field and send a verification email instead. Pre-select the country from the browser locale.

**Fitts's Law**: The primary button is small and bottom-left, away from where the eye and cursor finish.
→ Make "Create account" full width (or at least 44px tall) directly under the last field.

**Von Restorff Effect**: "Create account" and "Cancel" look identical, so nothing stands out.
→ Give the primary action the brand colour. Make Cancel a plain text link, or remove it.

**Jakob's Law**: Users expect social sign-in on modern SaaS signups.
→ Add "Continue with Google / Microsoft" above the form.

**Doherty Threshold**: A 3-second blank screen after submit feels broken.
→ Show a loading state on the button immediately and move the user on optimistically.

**Peak-End Rule**: The flow ends on an empty dashboard, which is a flat, forgettable finish.
→ End with a welcome screen and one clear first action ("Create your first project") or sample data.

**Aesthetic-Usability Effect**: The grey, cramped form feels unfinished, so users are less forgiving of the friction above.
→ Add spacing, field labels above inputs and a consistent visual style.

### Top 3 highest-impact changes

1. Cut the form to email + password (+ social sign-in). This removes most of the Hick's, Miller's and Tesler's issues in one move.
2. Make "Create account" a large, full-width, brand-coloured button and demote Cancel.
3. Replace the blank wait and empty dashboard with instant feedback and a welcome screen with one clear next step.
