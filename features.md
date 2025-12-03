## **1. Branching Strategy**

1. **Main branch (`main`)**

   * Always clean, stable, reflects production-ready code.
   * No direct pushes allowed — only merge via Pull Request from feature branches.

2. **Feature branches (`feature/...`)**

   * Each feature implements a specific part of the assignment.
   * Naming convention: `feature/<short-descriptive-name>`.
   * Examples:

     * `feature/project-structure` → Folder structure, `src/` setup.
     * `feature/homepage` → `index.html`, header, footer, navigation.
     * `feature/about-page` → `about.html`.
     * `feature/contact-page` → `contact.html`.
     * `feature/registration-form` → `registration.html` and form validation.
     * `feature/course-catalog` → `course-catalog.html`.
     * `feature/course-detail` → `course-detail.html`.
     * `feature/student-dashboard` → `student-dashboard.html`.
     * `feature/thank-you-page` → `thank.html`.
     * `feature/calculator` → `calculator.html` and `calculator-result.html`.
     * `feature/css-js` → Add styles and scripts for layout or interactive features.
     * `feature/performance-optimization` → Lazy loading, proper HTML semantics, accessibility.
     * `feature/documentation` → `docs/`, README updates, AI usage logs, validation reports.

3. **Pull Request Workflow**

   * Each feature branch is reviewed (by you or lab partner) before merging to `main`.
   * GitHub Actions workflow will automatically deploy merged `main` to `gh-pages` and create a release.

---

## **2. Suggested Order of Implementation**

Follow the assignment requirement order to reduce merge conflicts and dependencies:

1. **Project Setup & Structure**

   * Branch: `feature/project-structure`
   * Tasks:

     * Create `src/` folder with all HTML pages.
     * Create `css/`, `js/`, `images/`, `docs/` folders.
     * Configure logical filenames (`index.html`, etc.).
     * Add README with project overview and AI usage documentation.

2. **Homepage**

   * Branch: `feature/homepage`
   * Tasks:

     * Header, navigation, breadcrumb, main content with two-column layout.
     * Footer and social media links.
     * Featured courses, latest announcements, statistics section.

3. **About Page**

   * Branch: `feature/about-page`
   * Tasks:

     * Use `<section>`, `<dl>`, `<ol>`, `<ul>` for structured content.
     * Breadcrumb: `Home > About`.

4. **Contact Page**

   * Branch: `feature/contact-page`
   * Tasks:

     * Use `<address>` for university contact info.
     * Embedded map placeholder.
     * Breadcrumb: `Home > Contact Me`.

5. **Registration Form**

   * Branch: `feature/registration-form`
   * Tasks:

     * Semantic `<form>` with fieldsets for personal, academic, and course info.
     * Validation attributes (`required`, `pattern`, `minlength`, `maxlength`, `min`, `max`).
     * Accessibility: ARIA labels, logical tab order, autofocus, hidden fields.
     * Breadcrumb: `Home > Registration`.

6. **Course Catalog**

   * Branch: `feature/course-catalog`
   * Tasks:

     * Filters, sorting, table for courses, course thumbnails.
     * Semantic `<section>`, `<article>`, `<dl>` for course info.
     * Breadcrumb: `Home > Course Catalog`.

7. **Course Detail Page**

   * Branch: `feature/course-detail`
   * Tasks:

     * Detailed course info, syllabus, lessons, instructor info, reviews.
     * `<figure>` for images, `<time>` for dates, `<aside>` for recommended courses.

8. **Student Dashboard**

   * Branch: `feature/student-dashboard`
   * Tasks:

     * Overview of enrolled courses, progress stats.
     * Sections for recent activity, upcoming deadlines, achievements.

9. **Thank You Page**

   * Branch: `feature/thank-you-page`
   * Tasks:

     * Confirmation message, submitted info, next steps links.

10. **Calculator**

    * Branch: `feature/calculator`
    * Tasks:

      * Create `calculator.html` with scientific functions.
      * `calculator-result.html` shows results using `<dl>`.

11. **CSS and JS**

    * Branch: `feature/css-js`
    * Tasks:

      * Layout styles, responsiveness, interactive JS for navigation, calculator, etc.

12. **Performance & Validation**

    * Branch: `feature/performance-optimization`
    * Tasks:

      * Lazy load images, optimize HTML structure, validate all pages.
      * Document Core Web Vitals analysis.

13. **Documentation**

    * Branch: `feature/documentation`
    * Tasks:

      * Update `README.txt` with AI usage.
      * Add validation reports, website map, performance screenshots.

---

## **3. Implementation Notes**

* Each branch should be **small, focused, and complete for its feature**.
* After finishing a feature:

  1. Push the branch: `git push origin feature/<name>`.
  2. Create a **Pull Request to `main`**.
  3. Merge after reviewing.
* This ensures `main` is always clean, deployable, and ready for automatic GH Pages deployment and release.

