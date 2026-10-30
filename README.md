# CinePulse — Movie Explorer & Studio Dashboard

## 1. Your Mission: Investigate & Fix the Bugs

You are a **Full-Stack Developer** working on CinePulse, a movie discovery and studio management application. The QA team has identified several issues affecting the application's core functionality, including catalog filtering, pagination, watchlist management, and asynchronous search operations. Your responsibility is to investigate the existing codebase, trace each issue to its root cause, and implement reliable fixes while ensuring the application's existing functionality remains intact.

The following issues have been reported:

**BUG-01: Missing Movies at the Year Boundary**

The release year filter is excluding movies released in the maximum year selected. For example, selecting 2020–2024 fails to display some 2024 releases, including *Dune: Part Two* and *Challengers*.

**Your task:** Fix the year filtering logic to ensure both the minimum and maximum selected years are included.

**BUG-02: Incorrect Pagination Results**

The catalog is configured to display 6 movies per page, but only 5 are appearing. Additionally, the final movie in each page segment is being skipped during navigation.

**Your task:** Correct the pagination and array slicing logic to ensure every page displays the expected number of movies without skipping entries.

**BUG-03: Watchlist Removes the Wrong Movie**

When users remove a movie from their watchlist, the selected movie remains while another movie, typically the last entry, disappears instead.

**Your task:** Fix the removal logic so that the movie matching the selected ID is removed accurately.

**BUG-04: Search Gets Stuck After Failed Requests**

When an asynchronous search request fails due to a timeout or unexpected error, the application displays an error alert but remains stuck in the loading state. The search input stays disabled, preventing users from performing new searches.

**Your task:** Ensure the loading state is properly reset after both successful and failed requests, allowing users to continue searching.

---

## 2. Get Familiar With the Application

Before making any changes, explore CinePulse and understand how its different components interact.

CinePulse is an interactive movie discovery and curation dashboard designed for film enthusiasts and studio catalog managers.

**What the application offers:**

- **Movie Discovery:** Browse a catalog of highly rated movies with posters, genres, ratings, and descriptions.
- **Advanced Filtering:** Filter movies by genre, release year, and minimum rating.
- **Sorting:** Organize movies by rating or release date.
- **Personal Watchlist:** Save and remove movies with persistent offline storage.
- **Instant Search:** Search movies by title or director using debounced asynchronous queries.
- **Pagination:** Navigate through the movie catalog using structured page navigation.

**Technology Stack**

- React 18
- Vite 5
- Vanilla CSS
- Vitest
- React Testing Library
- jsdom
- Local JSON dataset (`data/movies.json`)

**Live Application Preview**



[INSERT SCREENSHOT: Movie Catalog with Filters and Search]

[INSERT SCREENSHOT: Watchlist Drawer]

---

## 3. Expected Behaviour After Fixing the Bugs

Once you have investigated and resolved all reported issues, CinePulse should behave as expected:

1. **Year Filtering:** Selecting 2020–2024 must include movies released in both 2020 and 2024.
2. **Pagination:** Every page must display up to 6 movies, with no missing or duplicated entries between pages.
3. **Watchlist:** Removing a movie must delete only the selected movie, identified by its unique ID.
4. **Search Recovery:** Failed search requests must reset the loading state and allow subsequent searches.
5. **Application Stability:** All existing functionality must continue working without regressions.

---

## 4. Your Workspace & Available Tools

You have access to a fully functional development workspace with the complete CinePulse source code, an integrated terminal, a live application preview, and an AI-powered coding assistant.

**Here's what you can do in your workspace:**

- **Explore the Codebase:** Navigate through the project files, inspect components, understand application logic, and identify where bugs originate.
- **Integrated Terminal:** Execute commands, install dependencies, start the development server, run tests, and inspect build errors.
- **Live Application Preview:** View CinePulse running in real time and verify whether your changes produce the expected behaviour.
- **AI Assistant:** Ask questions, understand unfamiliar code, investigate errors, and receive debugging guidance. Use it as a guide, not as a replacement for your own problem-solving.
- **Code Editing:** Modify existing files, refactor logic, and implement fixes directly within the workspace.
- **Test Execution:** Run automated test suites to validate your implementation and identify remaining issues.

**Useful Terminal Commands**

You can use the integrated terminal to execute commands such as:

| Command | Purpose |
|---|---|
| `npm run dev` | Start the development server |
| `npm test` | Execute automated tests (if configured) |

Check the project's `package.json` before executing commands to understand the available scripts.

**Hard Reset — Use Carefully**

The workspace includes a Hard Reset option that restores the challenge environment to its original state.

- You are allowed a maximum of **2 Hard Reset activations**.
- A minimum cooldown of **10 minutes** applies between consecutive activations.
- A reset discards your current code changes and restores the original challenge files.
- Use this option only when you genuinely need to restart your implementation.

**Remember:** Your objective is to understand the existing application and fix its underlying issues, not rebuild it from scratch.

---

## 5. Testing, Evaluation & Submission

Fixing the code is only half the job. You must verify that your implementation actually works.

**Before submitting:**

1. Reproduce the reported issues and understand their root causes.
2. Implement the necessary fixes in the existing codebase.
3. Run the available automated tests through the integrated terminal.
4. Check the live application preview to verify that the affected features work correctly.
5. Ensure your changes have not introduced regressions in existing functionality.

**Evaluation Criteria**

Your submission will be evaluated against automated test cases, including hidden test cases that are not visible during development.

- All four reported issues must be resolved.
- Both visible and hidden test cases must pass.
- Existing application functionality must remain intact.
- The application must build and execute successfully.

Once you are satisfied with your implementation, submit your solution through DEBUG//LAB.

**Your final score will reflect the correctness of your fixes and the results of the automated evaluation.**
