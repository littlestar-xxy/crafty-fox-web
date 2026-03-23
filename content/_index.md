---
title: 'SEISAD'
date: 2024-01-01
type: landing

design:
  spacing: "6rem"

sections:
  # 0. Logo Bar 
  - block: markdown
    content:
      title: ""
      subtitle: ""
      text: |
        <div style="display: flex; justify-content: space-between; align-items: center; width: 100%; max-width: 1200px; margin: 0 auto; padding: 20px 0;">
          <img src="media/chimie.png" style="height: 55px; width: auto;">
          <img src="media/iclehs.png" style="height: 80px; width: auto;">
          <img src="media/cnrs.png" style="height: 55px; width: auto;">
        </div>
        <div style="text-align: center; color: #555; font-style: italic; border-top: 1px solid #eee; padding-top: 15px; max-width: 1200px; margin: 0 auto;">
          — Institute of Chemistry for Life & Health Sciences —
        </div>
    design:
      columns: '1' 
      spacing:
        padding: ["1rem", 0, "1rem", 0]
  
  # 1. Group Photo
  - block: markdown
    content:
      title: ""
      subtitle: ""
      text: |
        <div style="width: 100%; max-width: 1200px; margin: 0 auto;">
          <img src="media/AA3A0511.JPG" style="width: 100%; height: auto; display: block; border-radius: 8px; box-shadow: 0 4px 12px rgba(0,0,0,0.1);">
        </div>
    design:
      columns: '1'
      spacing:
        padding: ["0", 0, "2rem", 0]
    
  # 3. Description
  - block: markdown
    content:
      title: "SEISAD"
      text: |
        <span style="float: left; font-size: 70px; line-height: 60px; padding-top: 4px; padding-right: 8px; font-family: Georgia;">A</span>ctually, the Team develops projects aimed at elaborating processes and tools for the early detection of pathological signals using chemical and analytical methodologies. The main prospections are related to: (i) new methodologies of synthesis and supported catalysis in mini – and continuous microflow reactors, synthesis of libraries of molecules as ligands of proteins, development of new radio-labelling methodologies for imaging; (ii) electrochemical sensors for biological systems and for screening biological markers, molecular materials for electroanalysis and electrocatalysis, microelectrochemical patterning of surfaces using scanning electrochemical microscopy, label-free electrochemical detection of microRNAs ; (iii) preparation of targeted optical and MR imaging agents, development of molecular magnetic resonance imaging MRI methods & functional imaging methods for the characterization and therapeutic follow-up of cancer in preclinics and (iv) characterization of new nano-supports and selective objects : peptide nanotubes, aptamers, nanobodies, design and characterization of original biocompatible nano-objects and quantitative characterization of their non-covalent interactions, development of miniaturized total analysis systems for applications ranging from environmental control to in-vitro medical diagnosis.
    design:
      spacing:
        padding: ["2rem", 0, "2rem", 0]
  
  # 4. Research Themes
  - block: features
    content:
      title: "Research Themes"
      items:
        - name: "Synthetic methodologies"
          description: "Development of new synthetic and/or radio-labelling methodologies"
          icon: flask
        - name: "Sensors"
          description: "Development of new electrochemical sensors"
          icon: bolt
        - name: "Imaging"
          description: "Development of new optical and MR imaging agents"
          icon: microscope
    design:
      columns: '1'
    

---
