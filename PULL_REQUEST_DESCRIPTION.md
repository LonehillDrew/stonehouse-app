## 🛒 Ecommerce Search & Filter Upgrade

This PR transforms the Stonehouse Café menu into a full ecommerce-style browsing experience.

### New Features

#### 🔍 Global Search
- Full-text search across all 150+ menu items
- Searches item name, description and category simultaneously
- Live results as you type with a clear (×) button

#### 🏷 Category Filter Chips
- Horizontal scrollable chip bar for all 12 menu categories
- One-tap to filter: Breakfast, Waffles, Burgers, Cocktails, G&T, Wine, Beer, Coffee, Milkshakes, Sweets, Kids, Cold Drinks
- "All" chip resets to full menu

#### ⚙️ Filter Drawer
Swipe-up panel with:
- **Category** — full section selector
- **Dietary & Tags** — Vegetarian 🥦, Popular ⭐, Spicy 🌶
- **Max Price slider** — drag to set price ceiling + preset buttons (Under R50 / R100 / R150 / Any)
- **Sort** — Default, Price ↑, Price ↓, A→Z, Popular First
- Reset and Apply buttons

#### 📌 Active Filters Bar
- Shows all active filters as removable tags
- Individual × to remove any single filter
- "Clear all" to reset everything

#### 🔢 Results Bar
- Live count of filtered results
- Sort dropdown always visible

#### 🛍 Product Grid (Ecommerce Style)
- Card grid: 2 col mobile → 3 col tablet → 4 col desktop → 5 col wide
- Category label on each card
- Popular badge on popular items
- Spicy indicator
- Green dot when item is in order
- Tap card image or name to open Quick View

#### 👁 Quick View Modal
- Full item details without leaving the browse page
- Add/remove quantity controls
- Save to favourites from within modal

#### ❤️ Favourites
- Heart button on every card
- Dedicated Saved tab with badge count
- Persists during session

#### 🛒 Order Page Improvements
- Emoji icon per line item (matches category)
- Name, table number and special requests form
- Clear entire order with confirmation guard
- Animated counter badge on tab

#### 🧾 Receipt
- Gold foil header strip
- Full line items with quantity and subtotal
- Customer details printed on slip
- "Please take your order to the counter" notice

### Bug Fixes
- Fixed `outerHTML` reassignment bug that broke qty buttons after first update
- Fixed HTML entity `&quot;` in `onclick` attributes
- All filter state managed cleanly without stale closures

### Files Changed
- `index.html` — complete rebuild (1,275 lines)
- `.github/workflows/deploy.yml` — updated to trigger on feature branch too
- `404.html` — redirect fallback added

---
*To merge: review, approve and squash-merge into `main`. GitHub Pages will auto-deploy.*
