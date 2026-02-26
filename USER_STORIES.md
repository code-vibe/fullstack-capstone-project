# GiftLink user stories

Use these stories with the `.github/ISSUE_TEMPLATE/user-story.md` template. Apply the `new` label on creation, then triage to `backlog` or `icebox` (optionally add `technical debt` when appropriate).

1. **Guest sign up and sign in**  
   As a guest, I want to create an account or sign in so that my activity is saved.  
   **Acceptance criteria:**  
   - Given I am on the auth page, when I submit valid credentials, then I land on the app with a visible signed-in state.  
   - When credentials are invalid, then I see an inline error without losing my input.  
   - When I click “Sign out,” then I am logged out and returned to the public landing page.

2. **Browse featured gifts**  
   As a shopper, I want to browse featured gifts so that I can discover items quickly.  
   **Acceptance criteria:**  
   - Given I open the landing page, then I see a grid of featured gifts with images and prices.  
   - When I scroll, additional featured gifts load without breaking layout.  
   - When I select a gift card, then I am taken to its details page.

3. **Search the catalog**  
   As a shopper, I want to search gifts by keyword so that I can find relevant items faster.  
   **Acceptance criteria:**  
   - Given I type a search term, then results update to include matching gifts.  
   - When no gifts match, then I see an empty state message.  
   - Search queries are debounced to avoid flooding the API.

4. **Filter and sort gifts**  
   As a shopper, I want to filter and sort gifts so that I can narrow to items that fit my needs.  
   **Acceptance criteria:**  
   - Given I select a filter (e.g., price range or category), then results update accordingly.  
   - When I choose a sort (e.g., price low-to-high), then the list reorders without losing filters.  
   - Clearing filters returns me to the unfiltered results.

5. **View gift details**  
   As a shopper, I want to view detailed information about a gift so that I can decide whether to buy or save it.  
   **Acceptance criteria:**  
   - Given I open a gift, then I see its name, description, price, and imagery.  
   - Related or recommended items are shown alongside the main details.  
   - A clear call-to-action lets me save the gift to my list.

6. **Save gifts to my list**  
   As a signed-in user, I want to save gifts so that I can revisit them later.  
   **Acceptance criteria:**  
   - Given I am signed in, when I click “Save,” then the gift is added to my list and persists across sessions.  
   - Removing a saved gift updates the list immediately.  
   - Attempting to save while signed out prompts me to sign in.

7. **Comment on gifts**  
   As a signed-in user, I want to leave comments on gifts so that I can share feedback with others.  
   **Acceptance criteria:**  
   - Given I am signed in, when I submit a comment, then it appears under the gift with my display name and timestamp.  
   - I can edit or delete my own comments.  
   - Attempting to comment while signed out prompts me to sign in.

8. **Manage profile and preferences**  
   As a signed-in user, I want to manage my profile and notification preferences so that my experience matches my needs.  
   **Acceptance criteria:**  
   - Given I open settings, then I can update profile details (name, email) and gift categories of interest.  
   - Preference changes save without requiring a page refresh.  
   - Notification settings persist across sessions and reflect on reload.

