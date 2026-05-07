# WAKAYAMA Travel App - Project Instructions

You are the primary developer for the WAKAYAMA Travel App. Follow these project-specific guidelines for all future modifications.

## 1. Design Philosophy & Style
- **Aesthetic**: Nordic Minimalist / WAKAYAMA style. Warm, earthy tones mixed with clean typography.
- **Colors**:
  - `dark`: #4F342E (Deep brown)
  - `accent`: #D98C5F (Warm orange)
  - `bg`: #F6F3E9 (Warm cream)
  - `card`: #E7E1D4 (Muted stone)
  - `text`: #332B2B (Rich charcoal)
- **Layout**: 
  - **Compact & Dense**: The itinerary view should remain compact (`gap-4`, smaller font sizes for metadata, etc.) to allow for easy scanning on mobile.
  - **Rounded Corners**: Use large border radii (`rounded-2xl`, `rounded-3xl`, `rounded-[1.5rem]`).
  - **Typography**: Clean sans-serif (Inter/Noto Sans TC) for UI, Serif (Playfair Display) for headers.

## 2. Shared Navigation & Components
- **Header**: Contains the "WAKAYAMA" brand, an information icon, and a **Train icon** link to Navitime Route Search (`https://japantravel.navitime.com/zh-tw/area/jp/route/`).
- **Icons**: Always use `lucide-react`.

## 3. Itinerary View (PlanTab)
- **Time Markers**: Use a vertical timeline line with a circular marker.
- **Map Integration**: Every itinerary item should have a Map icon (Lucide `MapIcon`). 
  - If a `mapUrl` exists, use it.
  - Otherwise, generate a Google Maps search link: `https://www.google.com/maps/search/?api=1&query=${encodeURIComponent(item.title)}`.
- **Item Styling**: Items use a left-border color accent matching their category (Transport, Activity, Restaurant, Shopping, etc.).

## 4. Feature Set
- **Itinerary Planning**: Add/Edit/Delete items and days.
- **Expense Tracking**: JPY to HKD conversion (Current rate stored in state, default ~0.052). Features split-bill tracking and image upload for receipts.
- **Checklist/Wishlist**: Shopping list and general "To-Do" tasks.
- **VJW QR Code**: Storage for Visit Japan Web QR code images.

## 5. Development Constraints
- **Compact UI**: Always prioritize a compact, mobile-friendly interface for the "Plan" view.
- **Icon-Only Buttons**: Use icons for common actions like "Map" or "Edit" to save horizontal space.
