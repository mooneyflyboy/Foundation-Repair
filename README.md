Below is a draft for a README.md file tailored for a GitHub repository, describing all the assumptions made in the foundation-repair.html tool. This README provides an overview of the tool, its purpose, and the specific assumptions behind its calculations and design, making it clear for users or contributors. The assumptions are drawn from the tool’s logic, pricing, and Texas-specific context as of April 11, 2025.
Texas Foundation Repair Estimator
Overview
The Texas Foundation Repair Estimator is a standalone HTML tool designed to estimate the number of piers and total cost for residential foundation repairs in Texas. It uses a simple, responsive interface with a Texas flag background, bright modern colors, and tooltips displayed in the bottom right of the input screen. Built as a single .html file, it runs locally in any modern browser (e.g., Safari, Chrome) without dependencies, making it easy to use on desktops or mobile devices.
Purpose
This tool provides homeowners or contractors with a quick, approximate cost estimate for foundation repairs, based on typical Texas residential conditions and average pricing as of April 11, 2025. It’s not a substitute for professional engineering quotes but serves as a starting point for planning.
Features
Inputs: Foundation Type, Square Footage, Repair Location, Severity, Pier Type, Depth, Access Difficulty, Optional Costs (Permits, Additional Repairs).
Output: A summary screen with a narrative breakdown of piers and costs.
Design: Texas flag background on input screen, mobile-optimized tooltips, bright colors (blue, coral, gray).
Usage: Open foundation-repair.html in a browser; no internet required if using a local flag image.
Assumptions
The tool’s calculations and design are based on the following assumptions, reflecting Texas residential repair practices and simplified modeling:
House Shape:
Assumes a square house for perimeter calculations. Perimeter = 
4 \times \sqrt{\text{square footage}}
.  
Example: 1,500 sq ft → 
\sqrt{1500} \approx 38.7
, 
4 \times 38.7 \approx 155
 ft.  
Rationale: Simplifies estimation; real homes vary (rectangular, L-shaped), but this approximates typical single-story Texas homes.
Pier Spacing and Density:
Slab Foundations (most common in Texas):
Perimeter: 1 pier every 6 feet. Example: 155 ft → 
155 / 6 \approx 26
 piers.  
Interior: 1 pier per 100 sq ft. Example: 1,500 sq ft → 
1500 / 100 = 15
 piers.  
Both: Perimeter (
perimeter / 6
) + Interior (
square footage / 200
). Example: 
26 + 7.5 \approx 34
 piers.
Crawl Space/Basement: 1 pier per 150 sq ft. Example: 1,500 sq ft → 
1500 / 150 = 10
 piers.  
Rationale: 6-ft spacing is a Texas contractor standard for slab perimeters due to clay soil movement. Interior and crawl/basement densities are lower, reflecting lighter support needs.
Severity Multipliers:
Light (1.0): Minor cracks (<1/4 inch), baseline piers.  
Moderate (1.5): Wider cracks (1/4-1/2 inch), 50% more piers.  
Severe (2.0): Large cracks (>1/2 inch), double piers.  
Rationale: Reflects increased stabilization needs with worsening damage, based on Texas repair trends.
Pier Costs:
Concrete: $1,100/pier (pressed pilings).  
Steel: $1,400/pier (deep-driven, durable).  
Helical: $2,000/pier (specialized for unstable soils).  
Rationale: Average 2025 Texas pricing, including materials and labor. Ranges align with industry norms ($1,000-$2,500/pier), adjusted for pier type complexity.
Depth Multipliers:
Shallow (1.0): Up to 10 ft, baseline cost.  
Medium (1.15): 10-20 ft, 15% more for typical Texas clay depth.  
Deep (1.4): Over 20 ft, 40% more for unstable soils.  
Rationale: Deeper piers require more materials and labor, common in Texas due to expansive clay soils.
Access Multipliers:
Easy (1.0): Clear site, no adjustment.  
Moderate (1.1): Landscaping obstacles, 10% more.  
Difficult (1.25): Tight spaces, 25% more.  
Rationale: Reflects additional labor/equipment costs, based on Texas contractor estimates.
Optional Costs:
Permits: $500 flat fee.  
Additional Repairs: $1,500 for cosmetic/drainage fixes.  
Rationale: Permits are typical in Texas municipalities (e.g., Houston); additional repairs are averaged from common extras like crack sealing or drainage.
Soil and Climate:
Assumes expansive clay soils (common in Texas), which shrink/swell with moisture, necessitating piers to stable layers.  
Rationale: Texas’s drought/rain cycles drive foundation issues, influencing pier depth and type.
Residential Focus:
Targets single-family homes with slab foundations (dominant in Texas).  
Rationale: Matches the state’s housing stock; commercial or multi-story buildings need different methods.
Simplification:
Costs are rounded to whole dollars.  
No regional price variation (e.g., Dallas vs. Houston).  
Ignores site-specific factors (e.g., soil tests, slope).  
Rationale: Keeps the tool user-friendly and broadly applicable, not a precise engineering model.
Design Assumptions:
Texas flag background uses an online SVG URL; assumes internet access unless replaced with a local image.  
Tooltips are hover-based; assumes desktop use or mobile hover simulation (not touch-optimized).  
Mobile layout assumes screens ≥320px wide.  
Rationale: Enhances Texas theme, prioritizes simplicity, and ensures responsiveness.
Usage
Local: Save foundation-repair.html, double-click to open in a browser (e.g., Chrome, Safari).  
Share: Host online (e.g., GitHub Pages, Google Drive) and send a URL for seamless browser access.  
Example: Upload to Drive, share link (https://drive.google.com/uc?id=[ID]), tap to open.
Offline: Replace flag URL with a local texas-flag.png in the same folder.
Limitations
Estimates are averages, not exact quotes.  
Assumes Texas conditions (clay soils, slab homes); less accurate elsewhere.  
No data persistence between sessions.  
Hover tooltips may not work on touch-only devices without modification.
Contributing
Fork this repo, adjust pricing/assumptions in the <script> section, or enhance mobile touch support. Pull requests welcome!
This README outlines all key assumptions, providing transparency for users and context for developers. You can copy this into a README.md file in your GitHub repo alongside foundation-repair.html. Let me know if you’d like to refine it further or need help setting up the repo!
