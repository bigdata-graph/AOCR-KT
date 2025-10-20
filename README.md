## Environment Setup

### Prerequisites
- Python 3.7+ (tested with Python 3.7)
- Required libraries (see `requirements.txt`)


## Dataset Description

### 1. ASSIST09
- **Full Name**: Assistment 2009-2010 Skill Builder Data  
- **Domain**: K-12 mathematics education (student-problem interaction data)  
- **Content**: Includes student response records (correctness, response time), problem-skill associations, etc.  
- **Download Links**:  
  - Raw dataset: [ASSIST09 Download](https://drive.google.com/file/d/1NNXHFRxcArrU0ZJSb9BIL56vmUt5FhlE/view)  
  - Official documentation: [ASSIST09 Docs](https://sites.google.com/site/assistmentsdata/home/assistment-2009-2010-data/skill-builder-data-2009-2010)  
- **Preprocessing**:  
  - Key steps: Filter empty skills, scaffolding problems, and users with few interactions; generate intermediate files such as problem-skill mappings and user interaction sequences.  


### 2. ASSIST12
- **Full Name**: Assistment 2012-2013 Data  
- **Domain**: K-12 mathematics education (extended version of ASSIST09)  
- **Features**: Larger dataset size; combined skills are separated by `$$$` (format difference from ASSIST09).  
- **Download Links**:  
  - Raw dataset: [ASSIST12 Download](https://drive.google.com/file/d/1uY8qG1gkxO73hXw8cBkg5L9hC94HhTgX/view)  
  - Official documentation: [ASSIST12 Docs](https://sites.google.com/site/assistmentsdata/home/assistment-2012-2013-data)  
- **Preprocessing**:  
  - Key steps: Same as ASSIST09; adapt parsing logic for combined skills to generate intermediate files in consistent formats (e.g., `pro_skill_sparse.npz`, `data.txt`).  


### 3. EdNet
- **Full Name**: EdNet: A Large-Scale Hierarchical Educational Dataset  
- **Domain**: Online education platform interaction data (covers multiple subjects)  
- **Subset**: Uses the `ednet-kt1` subset (dedicated to knowledge tracing tasks).  
- **Download Links**:  
  - Dataset: [ednet-kt1 Download](https://drive.google.com/file/d/1AmGcOs5U31wIIqvthn9ARqJMrMTFTcaw/view)  
  - Question info file: [Question Metadata Download](https://drive.google.com/file/d/117aYJAWG3GU48suS66NPaB82HwFj6xWS/view)  
  - Official repository: [EdNet GitHub](https://github.com/riiid/ednet)  
- **Preprocessing**:   
  - Key steps: Extract problem-skill mappings and user interaction sequences; calculate problem difficulty features (e.g., average response time, correctness rate).  


### Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/AOCR-KT.git
   cd AOCR-KT
   python AOCR_kt
