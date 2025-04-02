# **Fabric Draping Simulation Tool**  
*A Jupyter Notebook App for Solid-Mechanics Finite Element Analysis of Woven Fabrics*  

---

## **📌 Overview**  
This interactive Jupyter Notebook app simulates the draping of woven fabrics over a hemispherical mold using a **solid-mechanics finite element approach**, based on the paper:  
*"Solid-mechanics finite element simulations of the draping of fabrics: a sensitivity analysis" (Dong et al., 2000).*  

The tool allows users to explore the effects of key parameters (e.g., punch speed, material properties, friction) on fabric deformation, providing visualizations of **shear angle distribution** and **deformed fabric shape**.  

---

## **🚀 Features**  
✅ **Interactive Parameter Tuning**  
- Adjust punch speed, mesh size, material properties (shear & tensile moduli), friction coefficients, and holder force.  

✅ **Output Visualization**  
- **Shear Angle Plot**: Shows how shear varies along the fabric's diagonal.  
- **Deformation Plot**: Displays the draped fabric shape (hemisphere + flat rim).  

✅ **Physics-Based Approximations**  
- Empirical shear angle model derived from the paper.  
- Simplified FEM-like deformation for educational purposes.  

✅ **Educational Tool**  
- Helps understand the impact of numerical and material parameters on draping.  

---

## **📥 Installation**  
### **Prerequisites**  
- Python 3.8+  
- Jupyter Notebook / JupyterLab  
- Required Libraries:  
  ```bash
  pip install numpy matplotlib ipywidgets
  ```

### **Running the App**  
1. Clone this repository or download the `.ipynb` file.  
2. Open the notebook in Jupyter:  
   ```bash
   jupyter notebook Fabric_Draping_Simulation.ipynb
   ```
3. Run all cells to launch the interactive widget.  

---

## **🎮 Usage Guide**  
### **Adjustable Parameters**  
| Parameter | Description | Range | Default Value |
|-----------|-------------|-------|--------------|
| **Punch Speed** | Speed of the punch (m/s) | 0.1–100 | 30 m/s |
| **Mesh Size** | Number of elements (N×N) | 10, 30, 50, 70, 100 | 50×50 |
| **Shear Modulus (G₁₂)** | In-plane shear stiffness (Pa) | 7.8×10² – 7.8×10⁷ | 7.8×10⁴ |
| **Tensile Modulus (E₁₁)** | Tensile stiffness (Pa) | 7×10⁶ – 3.5×10¹⁰ | 3.5×10¹⁰ |
| **Friction (Punch/Fabric)** | Coefficient of friction | 0–1 | 0.2 |
| **Friction (Die/Fabric)** | Coefficient of friction | 0–1 | 0.5 |
| **Holder Force** | Force applied to holder (N) | 22–230,000 | 22,870 |

### **Expected Behavior**  
- **Low shear modulus** → More deformation in flat regions.  
- **High punch speed** → Potential numerical oscillations (if >30 m/s).  
- **High friction** → Smoother draping but may restrict motion.  
- **Excessive holder force** → Causes instability (wrinkling).  

---

## **📊 Output Interpretation**  
### **1. Shear Angle Distribution**  
- **X-axis**: Normalized distance from the apex (`L/S`).  
- **Y-axis**: Shear angle (degrees).  
- **Key Observation**:  
  - Maximum shear occurs at `L/S = 1` (edge of the hemisphere).  
  - Oscillations at `L/S > 1.5` indicate potential wrinkling.  

### **2. Deformed Fabric Shape**  
- **Color Map**: Height of the draped fabric.  
- **Hemisphere (Center)**: High curvature → Dominated by shear deformation.  
- **Flat Rim (Outer)**: Sensitive to friction & holder force.  

### **3. Output Example**  
![image](https://github.com/user-attachments/assets/10ce155a-516d-4273-af58-bdd7803607e1)

---

## **🔧 Extending the Model**  
For a **full FEM simulation**, consider:  
1. **Integrating ABAQUS/Explicit** (as used in the paper).  
2. **Adding Nonlinear Material Models** (e.g., hyperelasticity for rubbery fabrics).  
3. **Experimental Validation** (using friction data from Appendix A).  

---

## **📜 References**  
- Dong, L., Lekakou, C., & Bader, M. G. (2000). *Solid-mechanics finite element simulations of the draping of fabrics: a sensitivity analysis.* Composites Part A, 31(6), 639–652.  


---


---

**🎉 Happy Simulating!** 🎉
