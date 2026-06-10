# Epic 13: Responsive UI Polish

## Metadata
- **Epic ID:** EPIC-13
- **Priority:** P2 — Polish
- **Phase:** 3
- **Depends On:** All other epics (do last)
- **Estimated Effort:** Medium
- **Affected Apps:** ALL templates, CSS
- **Status:** `[ ] Not Started`

---

## Goal
Ensure the entire UI works properly on mobile browsers (≥320px) without needing a native app.

---

## Stories

### Story 13.1: Mobile-Responsive Sidebar
- **ID:** EPIC-13-S1
- **Status:** `[ ] Not Started`

#### Tasks
- `[ ]` Add hamburger toggle button for mobile (visible only on `sm` and below)
- `[ ]` Sidebar collapses off-canvas on mobile, slides in on hamburger click
- `[ ]` Use Bootstrap offcanvas or custom CSS for sidebar toggle
- `[ ]` Close sidebar when a link is clicked on mobile
- `[ ]` Ensure overlay/backdrop when sidebar is open on mobile

#### Acceptance Criteria
- [ ] Sidebar hidden by default on mobile
- [ ] Hamburger icon visible on mobile
- [ ] Sidebar slides in/out smoothly
- [ ] Links work and close sidebar on mobile

#### Files to Modify
- `dashboard/templates/dashboard/partials/_sidebar.html`
- `dashboard/templates/dashboard/dashboard.html`
- CSS (base or dedicated responsive CSS)

---

### Story 13.2: Responsive Data Tables
- **ID:** EPIC-13-S2
- **Status:** `[ ] Not Started`

#### Tasks
- `[ ]` Wrap all `<table>` elements in `<div class="table-responsive">` containers
- `[ ]` Audit all table-heavy pages:
  - Receptionist dashboard (appointment table)
  - Admin user list
  - Patient list (new)
  - Billing dashboard (new)
  - Payment history
  - Consultation list
- `[ ]` Ensure table columns don't break on small screens
- `[ ]` Consider hiding less important columns on mobile with `d-none d-md-table-cell`

#### Acceptance Criteria
- [ ] All tables horizontally scrollable on mobile
- [ ] No layout breaking on narrow viewports
- [ ] Critical data always visible

#### Files to Modify
- Multiple template files containing `<table>` elements

---

### Story 13.3: Mobile Booking Wizard
- **ID:** EPIC-13-S3
- **Status:** `[ ] Not Started`

#### Tasks
- `[ ]` Test booking wizard on mobile viewport
- `[ ]` Fix any layout issues:
  - Doctor cards stack vertically on mobile
  - Date picker fits screen width
  - Slot selection buttons are touch-friendly (min 44px tap targets)
  - Confirmation modal fits mobile screen

#### Acceptance Criteria
- [ ] Full booking flow works on 320px viewport
- [ ] All buttons/inputs touch-friendly
- [ ] Modals display properly on mobile

#### Files to Modify
- `dashboard/templates/patients/booking_wizard.html`
- Related CSS

---

### Story 13.4: Mobile Modal & Form Polish
- **ID:** EPIC-13-S4
- **Status:** `[ ] Not Started`

#### Tasks
- `[ ]` Audit all modals for mobile compatibility:
  - Cancellation modal
  - Reschedule modal
  - Status update modal
- `[ ]` Ensure modals are full-width on mobile (`modal-fullscreen-sm-down`)
- `[ ]` Ensure all form inputs are properly sized on mobile
- `[ ]` Test all forms on mobile viewport

#### Acceptance Criteria
- [ ] All modals work on mobile
- [ ] Form inputs are readable and touch-friendly
- [ ] No content hidden behind keyboard on mobile

#### Files to Modify
- Various template files containing modals and forms

---

## Definition of Done
- [ ] All 4 stories completed
- [ ] UI tested on 320px, 375px, 768px viewports
- [ ] No horizontal scroll on any page (except data tables within their scroll container)
- [ ] All interactive elements have ≥44px touch targets
- [ ] Sidebar toggle works on mobile
- [ ] Existing tests pass
