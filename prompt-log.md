# AgriRoot Marinduque — Prompt Engineering Log
**Course:** Web Systems and Technologies  
**Institution:** Marinduque State University  

---

## Task 1 — Sector Selection

*   **Sector:** Agriculture & Food Innovation
*   **Local Challenge:** Small-scale arrowroot (*urut*) farmers in Marinduque struggle to estimate optimal harvest dates and lack a direct frontend platform to showcase their products to buyers.
*   **Target Users:** Marinduque arrowroot farmers and local agri-cooperatives.
*   **Proposed Project:** AgriRoot Marinduque
*   **Key Features:** Harvest tracker calculator, interactive product showcase card grid, and a cooperative directory filter.

---

## Task 2 — Zero-Shot Prompting

**Objective:** Observe what Copilot generates from a basic prompt without any context or examples.

**Exact Prompt:**
> Create a simple webpage for an agricultural tracker and product showcase for Marinduque arrowroot farmers.

**Actual Copilot Output:**
*(A basic HTML file containing a static table for crop schedules, text paragraphs about arrowroot cookies, and an unstyled heading layout.)*

**What Worked:**
*   Generated a clean HTML shell structure with headers and sections.
*   Included basic placeholders for agricultural data.

**What Needs Improvement:**
*   The design was unstyled and completely non-responsive.
*   The tracker component was entirely static text and lacked JavaScript functionality.
*   Did not align with specific local cooperative requirements or layout structure.

**Next Action / Verification:**
Rewrite the prompt using the complete Anatomy of a Prompt structure to enforce responsive layout and JavaScript calculations.

---

## Task 3 — Structured Prompt Improvement

**Objective:** Apply Role, Task, Context, Constraints, and Expected Output to refine structural quality.

**Exact Prompt:**
> Act as an expert frontend web developer. Create a responsive single-page web interface named "AgriRoot Marinduque" using semantic HTML5, modern CSS, and vanilla JavaScript. No external frameworks or backend databases are allowed. 
> The page must include:
> 1. A Hero section celebrating Marinduque's Arrowroot industry.
> 2. An interactive Harvest Cycle Tracker form where a farmer inputs a planting date, and JS calculates the exact harvest range (8 to 10 months later).
> 3. A product showcase section displaying product cards with interactive filter buttons.
> Ensure the interface works seamlessly on mobile devices, maintains clear visual hierarchy, and remains readable.

**Actual Copilot Output:**
*(Generated an structured HTML5 layout with embedded CSS Flexbox rules and an operational JavaScript event listener computing harvest dates.)*

**Comparison with Initial Output:**
*   **Visual Structure:** Changed from a raw text page into a fully styled dashboard interface with a green agricultural color scheme.
*   **Functionality:** Upgraded the static text placeholders into a working computational tool powered by client-side JavaScript.

---

## Task 4 — Few-Shot and Role Assignment

### Experiment A: Few-Shot Prompting
**Objective:** Provide structural data formatting examples to achieve highly consistent card components.

**Exact Prompt:**
> Generate custom product cards for our product showcase grid using this exact layout format:
> Example 1:
> - Name: Traditional Arrowroot Cookies
> - Category: Food
> - Description: Authentic leaf-printed delicacies.
> 
> Generate two more items following this exact schema for 'Raw Tuber Flakes' and 'Organic Arrowroot Flour'.

**Actual Copilot Output:**
*(Copilot cleanly formatted the additional objects matching the exact HTML pattern provided in the prompt examples.)*

**Observation:** Few-shot examples completely eliminated stray formatting variants, keeping the grid completely uniform.

### Experiment B: Role Assignment
**Objective:** Leverage a specialized professional perspective to uncover hidden accessibility problems.

**Exact Prompt:**
> Act as a frontend accessibility reviewer. Examine our custom interactive form fields and checklist nodes. Identify code flaws regarding keyboard access, color contrast, and aria-labels. Recommend minor target remedies within raw frontend scope.

**Actual Copilot Output:**
*(Recommended explicitly binding `<label>` elements via `for` attributes to inputs and adding explicit `:focus` outline treatments to buttons.)*

**Observation:** Role assignment successfully spotlighted functional deficits that a typical layout engineer might skip over.

---

## Task 5 — Structured Analysis and Refinement

**Objective:** Request a rigorous checklist audit to correct semantic markup omissions.

**Exact Prompt:**
> Review our interactive prototype code. Check if form fields have semantic accessibility and whether layout elements flex appropriately on narrow screens. Provide a rapid technical fix for the single largest point of failure.

**Actual Copilot Output:**
*(Identified that the harvest tracker date inputs lacked dedicated ARIA aria-live regions for dynamic error status feedback and output values.)*

**Correction Implemented:** Enhanced input nodes with accessible labeling and explicitly coupled calculations to live output tags.

---

## Task 6 — Final Comparison and Reflection

### Comparison Table

| Technique | Observation |
| :--- | :--- |
| **Zero-Shot** | Produced generic skeletons lacking brand design, interactive utilities, or responsive layout frameworks. |
| **Structured Prompt** | Brought rigorous layout alignment, established custom styling rules, and added native JavaScript engine capabilities. |
| **Few-Shot** | Created consistent item card data structures matching specific contextual themes without pattern drifting. |
| **Role Assignment** | Sparked deep architectural audits exposing crucial focus properties and semantic web accessibility updates. |
| **Structured Analysis** | Verified exact component alignments, optimized code logic, and fixed minor structural flaws. |

### Final Reflection
Structured prompting provided an elite starting point by defining exact design limits right out of the gate. I learned that prompt engineering is an iterative, step-by-step conversation. While AI speeds up frontend creation, human review remains vital to ensure semantic correctness and true accessibility.
