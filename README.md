# Dynamo---Renumbering-of-Sheets

This automation tool for Autodesk revit allows hte re-numbering of a specific set of sheets previously selected by the user from the Project Browser. 
The tool addresses the "duplicate number" conflict in Revit through a three-step execution logic: 

##Phase 1: Selection and Ordering
The routine begins by capturing the selection from the Prohect Browser. These elements are stored in a list and sorted via a custom function. The sorting logid is strictly dictated by the current **Sheet Number**, ensuring a predictable sequence before any modification occurs. 

##Phase 2: Temporary Renaming (Conflict Resolution) 
Revit doesn't allow to use a Sheet Number that is already in use by another element. To bypass this constraint, the tool implements a temporary naming phase with a placeholder value which frees up the namespace for the final sequence. 

##Phase 3: Definitive Numbering 
Once the namespace is cleared, the tool executes the final assignment of the new Sheet Numbers. 



## Technical Implementation
* **Platform:** Autodesk Revit
* **API Interaction:** Revit API / Dynamo
* **Key Logic:** * Element selection via UI.
    * List sorting algorithms.
    * Parameter management for Namespace conflict resolution.


