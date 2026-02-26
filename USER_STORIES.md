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

## Project delivery user stories

1. **Finish user stories**  
   **As a** product owner  
   **I need** a complete set of user stories covering the GiftLink roadmap  
   **So that** the team can plan sprints with clarity and priority  
   ### Details and Assumptions  
       * Stories are captured in this repository and follow the shared template  
       * Stories include clear acceptance criteria for engineering and QA  
   ### Acceptance Criteria  
       gherkin  
       Given the backlog grooming meeting  
       When the user story set is reviewed  
       Then all ten roadmap stories are present, templated, and ready for prioritization

2. **Initialize and populate MongoDB**  
   **As a** backend developer  
   **I need** MongoDB initialized with seed collections and sample data  
   **So that** the application can run locally and in CI with predictable fixtures  
   ### Details and Assumptions  
       * Environment variables for MongoDB connection are documented  
       * A seed script creates required collections and inserts baseline data  
   ### Acceptance Criteria  
       gherkin  
       Given a fresh environment with configured MongoDB credentials  
       When I run the database setup and seed scripts  
       Then the required collections exist with baseline gift and user data available to the app

3. **Run skeleton application**  
   **As a** full-stack developer  
   **I need** the skeleton backend and frontend to start successfully  
   **So that** I can validate wiring before feature implementation  
   ### Details and Assumptions  
       * README documents commands to start backend and frontend services  
       * Health endpoints or landing routes respond without runtime errors  
   ### Acceptance Criteria  
       gherkin  
       Given the codebase is installed with dependencies  
       When I start the skeleton application using documented commands  
       Then backend and frontend processes run without critical errors and expose their health routes

4. **Implement a landing page and navigation**  
   **As a** visitor  
   **I need** a landing page with clear navigation  
   **So that** I can understand the product and reach key areas quickly  
   ### Details and Assumptions  
       * Navigation links include search, featured gifts, and authentication entry points  
       * Landing page content highlights value proposition and primary CTA  
   ### Acceptance Criteria  
       gherkin  
       Given I open the site root  
       When the landing page loads  
       Then I see hero content with a primary CTA and navigation links to Gifts, Search, and Sign In/Up

5. **Add authentication components and logic**  
   **As a** returning user  
   **I need** sign-up and sign-in flows with session handling  
   **So that** I can access personalized features securely  
   ### Details and Assumptions  
       * Auth UI supports email/password and shows validation errors inline  
       * Tokens or sessions are stored securely and sign-out clears them  
   ### Acceptance Criteria  
       gherkin  
       Given I am on the authentication page  
       When I submit valid credentials  
       Then I am signed in, see my user state, and can sign out to clear the session

6. **Implement Gifts details page**  
   **As a** shopper  
   **I need** a detailed view for each gift  
   **So that** I can evaluate the item and take action  
   ### Details and Assumptions  
       * Page displays name, description, price, imagery, and availability  
       * Primary actions include saving or sharing the gift  
   ### Acceptance Criteria  
       gherkin  
       Given I select a gift from listings  
       When I open its details page  
       Then I see the gift’s core details and a clear call-to-action to save or share

7. **Implement a search component**  
   **As a** shopper  
   **I need** to search gifts by keyword  
   **So that** I can find relevant items quickly  
   ### Details and Assumptions  
       * Search input debounces queries and handles empty states  
       * Results display matching gifts with key fields (title, price, image)  
   ### Acceptance Criteria  
       gherkin  
       Given I enter a search term  
       When results are fetched  
       Then matching gifts are shown, and no-results messaging appears when nothing matches

8. **Design and implement the comments feature**  
   **As a** signed-in user  
   **I need** to post and manage comments on gifts  
   **So that** I can share feedback with other shoppers  
   ### Details and Assumptions  
       * Comment submission requires authentication and shows error states  
       * Users can edit or delete their own comments; timestamps are displayed  
   ### Acceptance Criteria  
       gherkin  
       Given I am signed in on a gift details page  
       When I submit a comment  
       Then it appears with my name and timestamp, and unauthenticated users are prompted to sign in before commenting

9. **Containerize the services and applications**  
   **As a** DevOps engineer  
   **I need** container images for backend and frontend  
   **So that** environments are consistent across local, CI, and production  
   ### Details and Assumptions  
       * Dockerfiles exist for backend and frontend with documented build args  
       * A compose file or equivalent runs services together locally  
   ### Acceptance Criteria  
       gherkin  
       Given the repository Dockerfiles  
       When I build images using the documented commands  
       Then backend and frontend images build successfully and run via compose with expected ports exposed

10. **Deploy backend and frontend**  
    **As a** release manager  
    **I need** automated deployment of backend and frontend  
    **So that** users can access the latest stable version reliably  
    ### Details and Assumptions  
        * Deployment targets are defined with environment variables managed securely  
        * CI/CD pipeline publishes artifacts and promotes builds to staging and production  
    ### Acceptance Criteria  
        gherkin  
        Given a successful build of backend and frontend  
        When the deployment pipeline runs  
        Then the APIs and web app are reachable at their target URLs with environment configuration applied
