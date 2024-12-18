In React Native (and CSS Flexbox), alignItems and justifyContent are used to control the layout of child elements within a container. They behave differently depending on whether they are applied to the cross-axis or main-axis of the container.

---

Here’s a summary table for **`alignItems`**, which aligns child elements along the **cross-axis** in a Flexbox layout:

---

### **Summary Table for `alignItems`**

| **Value**          | **Effect**                                                                  |
|---------------------|----------------------------------------------------------------------------|
| **`flex-start`**    | Aligns items at the **start** of the cross-axis (top for `row`, left for `column`). |
| **`center`**        | Aligns items at the **center** of the cross-axis.                          |
| **`flex-end`**      | Aligns items at the **end** of the cross-axis (bottom for `row`, right for `column`). |
| **`stretch`** (Default) | Stretches items to **fill** the container along the cross-axis (if no size is specified). |
| **`baseline`**      | Aligns items so their **text baselines** align (useful for text-heavy layouts). |

---

### **Descriptions**

1. **`flex-start`**  
   - Child elements are aligned at the beginning of the cross-axis.
   - For `flexDirection: 'row'`, this aligns items at the **top**.
   - For `flexDirection: 'column'`, this aligns items at the **left**.

2. **`center`**  
   - Child elements are aligned at the center of the cross-axis.
   - For both directions (`row` or `column`), items are centered perpendicularly to the main axis.

3. **`flex-end`**  
   - Child elements are aligned at the end of the cross-axis.
   - For `flexDirection: 'row'`, this aligns items at the **bottom**.
   - For `flexDirection: 'column'`, this aligns items at the **right**.

4. **`stretch`**  
   - Child elements stretch to fill the container along the cross-axis, as long as no specific size (height for `row`, width for `column`) is set.
   - This is the default value for `alignItems`.

5. **`baseline`**  
   - Child elements are aligned such that their **text baselines** are lined up.
   - This is particularly useful when dealing with mixed text and other visual elements.

---

### Visual Example (Cross-Axis Behavior)

#### **`flexDirection: 'column'`**
- **Cross-Axis:** Horizontal  
- Values affect **horizontal alignment**.

| **Value**          | **Effect**                         |
|---------------------|------------------------------------|
| **`flex-start`**    | Align left                        |
| **`center`**        | Align center horizontally         |
| **`flex-end`**      | Align right                       |
| **`stretch`**       | Fill horizontal width             |
| **`baseline`**      | Align text baselines horizontally |

#### **`flexDirection: 'row'`**
- **Cross-Axis:** Vertical  
- Values affect **vertical alignment**.

| **Value**          | **Effect**                         |
|---------------------|------------------------------------|
| **`flex-start`**    | Align top                         |
| **`center`**        | Align center vertically           |
| **`flex-end`**      | Align bottom                      |
| **`stretch`**       | Fill vertical height              |
| **`baseline`**      | Align text baselines vertically   |

---

## Here are the commonly used values for `justifyContent` in React Native (and CSS Flexbox), along with their descriptions:

---

### **1. `flex-start` (Default)**
- **Description:** 
  Aligns all child elements at the **beginning** of the main axis (top for `flexDirection: 'column'` and left for `flexDirection: 'row'`).
- **Example:** Items are stacked from the top (or start) with no space in between.

---

### **2. `center`**
- **Description:** 
  Aligns all child elements at the **center** of the main axis.
- **Example:** Items are stacked in the middle of the container along the main axis.

---

### **3. `flex-end`**
- **Description:** 
  Aligns all child elements at the **end** of the main axis (bottom for `flexDirection: 'column'` and right for `flexDirection: 'row'`).
- **Example:** Items are stacked at the bottom (or end) with no space in between.

---

### **4. `space-between`**
- **Description:** 
  Distributes child elements evenly along the main axis with **equal space** between them, but **no space** at the start or end.
- **Example:** Items are spread apart evenly, touching the container's edges at the start and end.

---

### **5. `space-around`**
- **Description:** 
  Distributes child elements with **equal space around them**. This means the space between items is twice the space at the start and end.
- **Example:** Items have padding-like spacing on both sides, resulting in a balanced layout with space before the first and after the last item.

---

### **6. `space-evenly`**
- **Description:** 
  Distributes child elements with **equal space between and around them**, ensuring uniform spacing throughout.
- **Example:** Items have the same amount of space between them as at the container's edges.

---

### Summary Table

| **Value**         | **Effect**                                                                  |
|--------------------|----------------------------------------------------------------------------|
| **`flex-start`**   | Aligns items at the start of the main axis.                                |
| **`center`**       | Aligns items at the center of the main axis.                               |
| **`flex-end`**     | Aligns items at the end of the main axis.                                  |
| **`space-between`**| Equal spacing **between** items, none at the edges.                        |
| **`space-around`** | Equal spacing **around** items, edges have half the spacing as between.    |
| **`space-evenly`** | Equal spacing **between and around** items, including at the edges.        |
