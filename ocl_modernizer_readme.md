# OCL Reference Modernizer

A Jupyter notebook tool that modernizes OCL (Open Concept Lab) collection references by converting versioned references to unversioned equivalents.

**GitHub Issue**: [#2212](https://github.com/OpenConceptLab/ocl_issues/issues/2212)

## 🎯 What It Does

- **Analyzes** OCL collection export files to identify versioned references
- **Converts** versioned references (e.g., `/concepts/123/456789/`) to unversioned (`/concepts/123/`)
- **Generates** bulk import files for OCL API to apply changes
- **Preserves** unversioned references unchanged
- **Prevents** duplicate expressions
- **Supports** cascade configuration presets (OpenMRS, custom, etc.)

## 🚀 Quick Start

1. **Export** your OCL collection to JSON format
2. **Open** `ocl_modernizer_notebook.ipynb` in Jupyter
3. **Configure** the input file path and settings in Step 2
4. **Run** all cells sequentially
5. **Review** generated files before importing to OCL

## 📁 Generated Files

- `unversioned_references_*.json` - New unversioned references to add
- `references_to_delete_*.json` - Versioned references to remove ⚠️ **Import this FIRST**
- `migration_report_*.txt` - Detailed statistics and instructions

## ⚙️ Key Features

- **Smart Processing**: Only modernizes versioned references
- **Duplicate Detection**: Prevents duplicate expressions  
- **Cascade Presets**: OpenMRS, custom, or no cascade options
- **Comprehensive Reporting**: Detailed statistics and validation
- **Safe by Default**: Preserves original references structure

## ⚠️ Important Reminders

1. **Backup first** - Create a collection version before importing
2. **Test first** - Try on a test collection before production  
3. **Order matters** - Import deletions before additions
4. **Validate results** - Check collection expansions after migration

## 📊 Typical Results

- Converts all versioned references to unversioned equivalents
- Maintains cascade settings and reference structure and can apply new cascade parameters
- Reports detailed statistics on changes made

---

*For detailed instructions and examples, see the notebook cells. All configuration and processing happens within the Jupyter notebook interface.*