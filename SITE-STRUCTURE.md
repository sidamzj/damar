# Vue Project Structure

This guide explains the current website structure so you can customize it with confidence.

---

## 1. Entry points

- `src/main.js`
  - Creates the Vue app.
  - Imports `App.vue`, the router, and global styles from `src/style.css`.

- `src/App.vue`
  - Contains only `<router-view />`.
  - This means page content is determined by Vue Router.

- `src/router/index.js`
  - Defines the routes used by the app.
  - Current routes:
    - `/` -> `LandingPage.vue`
    - `/login` -> `LoginPage.vue`

> Important: `HelloWorld.vue` is not referenced by the router, so editing it will not change the site unless you wire it into `router/index.js` or another component.

---

## 2. Main pages

### `src/components/LandingPage.vue`
This is the actual homepage component shown at `/`.
It contains the landing page layout and main sections directly in its template.

To customize the homepage content, update this file.

### `src/components/LoginPage.vue`
This is the login page shown at `/login`.
It includes:
- email and password inputs
- login button
- social login placeholders
- a side panel with marketing text

Customize the login flow and text here.

---

## 3. Other page components

### `src/components/HelloWorld.vue`
- This component composes lots of sections (`Navbar.vue`, `HeroSection.vue`, `PromoSection.vue`, `KeunggulanSection.vue`, `PricingSection.vue`, `FAQSection.vue`, `Footer.vue`).
- It is currently unused by the router.
- If you want to make a new homepage layout using these sections, you can connect `HelloWorld.vue` in `src/router/index.js`.

Example routing change:
```js
import HelloWorld from '../components/HelloWorld.vue'

const routes = [
  { path: '/', component: HelloWorld },
  { path: '/login', component: LoginPage },
]
```

### Reusable sections
The project includes these section components:
- `Navbar.vue` — navigation bar and header links
- `HeroSection.vue` — hero content, promo buttons, hero image
- `PromoSection.vue` — promo cards section
- `KeunggulanSection.vue` — feature/benefits section
- `PricingSection.vue` — pricing cards section
- `FAQSection.vue` — frequently asked questions section
- `Footer.vue` — footer content
- `PricingCard.vue` and `PromoCard.vue` — smaller reusable card components used by the pricing and promo sections

---

## 4. Styling and assets

- `src/style.css`
  - Global CSS styles for the project.
  - Tailwind utilities are used plus custom classes.

- `tailwind.config.js`
  - Tailwind CSS configuration.
  - Controls theme, screens, plugins, and other Tailwind options.

- `public/`
  - Static assets served directly.
  - Put images or files here if you want them available at build time.

- `src/assets/`
  - Local image assets imported into Vue components.
  - Example: `HeroSection.vue` imports `hero.png`.

---

## 5. How to customize the site

1. Decide which page you want to change:
   - Homepage: edit `src/components/LandingPage.vue`.
   - Login page: edit `src/components/LoginPage.vue`.
   - New homepage with section components: use `src/components/HelloWorld.vue` and update `src/router/index.js`.

2. If you want to add or change sections:
   - Create a new component in `src/components/`
   - Import it into the page component
   - Add it to the template

3. If you want to change navigation:
   - Edit `Navbar.vue`
   - Or replace the navbar inside `LandingPage.vue` / `HelloWorld.vue`

4. Update text, buttons, images, or page layout directly in the component templates.

---

## 6. Quick tips

- If changes do not appear, ensure the changed file is actually used by the route.
- Use `router/index.js` to point a route to a different component.
- If you want the app to use `HelloWorld.vue` as homepage, swap the route component for `/`.
- For layout changes, edit the template sections and class names in the relevant `.vue` file.

---

## 7. Common customization examples

- Change homepage headline:
  - edit `LandingPage.vue` and replace the text in the hero section.

- Add a new section:
  - create `src/components/NewSection.vue`
  - import it into `LandingPage.vue`
  - add `<NewSection />` inside the page template.

- Use Tailwind classes:
  - modify class attributes in the templates
  - update `style.css` for custom utilities

---

## 8. Notes

- The app is a Vue 3 app using Vite and Vue Router.
- Routes are the main way pages are switched.
- Unused components like `HelloWorld.vue` can still be useful as a page template if you connect them.

Happy customizing!