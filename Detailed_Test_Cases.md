
# Detailed Test Cases for CSOP Background

---

## **1. Fund Information Management**

### Test Case 1: Create a New Fund  
| **Test Case ID** | TC_FIM_001                             |
|-------------------|---------------------------------------|
| **Description**   | Verify that a new fund can be created successfully. |
| **Precondition**  | User has appropriate permissions to add funds. |
| **Test Steps**    | 1. Navigate to the "Create Fund" page.<br>2. Enter valid fund details (name, ticker, inception date, etc.).<br>3. Click "Save." |
| **Expected Result** | The fund is successfully created and listed in the fund database. |
| **Priority**      | High                                  |
| **Test Data**     | Fund Name: Alpha Growth Fund<br>Ticker: AGF |

---

### Test Case 2: Edit Fund Details  
| **Test Case ID** | TC_FIM_002                             |
|-------------------|---------------------------------------|
| **Description**   | Verify that fund details can be updated. |
| **Precondition**  | Fund already exists in the system.    |
| **Test Steps**    | 1. Navigate to the "Edit Fund" page.<br>2. Modify details such as investment objective.<br>3. Click "Save." |
| **Expected Result** | Updates are successfully saved and displayed. |
| **Priority**      | Medium                                |
| **Test Data**     | Updated Investment Objective: Long-term capital appreciation. |

---

### Test Case 3: Delete a Fund  
| **Test Case ID** | TC_FIM_003                             |
|-------------------|---------------------------------------|
| **Description**   | Verify that an existing fund can be deleted. |
| **Precondition**  | Fund exists in the system, and the user has deletion permissions. |
| **Test Steps**    | 1. Navigate to the fund list.<br>2. Select a fund.<br>3. Click "Delete" and confirm the action. |
| **Expected Result** | The fund is successfully removed from the system. |
| **Priority**      | High                                  |

---

## **2. Performance Tracking**

### Test Case 4: Calculate TWR  
| **Test Case ID** | TC_PT_001                              |
|-------------------|---------------------------------------|
| **Description**   | Validate the accuracy of the Time-Weighted Return calculation. |
| **Precondition**  | Fund has valid performance data.      |
| **Test Steps**    | 1. Navigate to the performance metrics page.<br>2. Select a fund.<br>3. Verify the displayed TWR. |
| **Expected Result** | The TWR value is accurate and consistent with the input data. |
| **Priority**      | High                                  |

---

### Test Case 5: Generate Performance Report  
| **Test Case ID** | TC_PT_002                              |
|-------------------|---------------------------------------|
| **Description**   | Verify that performance reports can be generated. |
| **Precondition**  | Fund has sufficient performance history. |
| **Test Steps**    | 1. Select a fund.<br>2. Click "Generate Report." |
| **Expected Result** | The report is generated and includes metrics like Sharpe and Sortino Ratios. |
| **Priority**      | Medium                                |

---

## **3. Holding Information Management**

### Test Case 6: Add a New Security to Holdings  
| **Test Case ID** | TC_HIM_001                             |
|-------------------|---------------------------------------|
| **Description**   | Verify that new securities can be added to fund holdings. |
| **Precondition**  | User has permissions to modify holdings. |
| **Test Steps**    | 1. Navigate to the "Add Holdings" page.<br>2. Enter security details.<br>3. Click "Add." |
| **Expected Result** | The security is added, and portfolio weights are updated. |
| **Priority**      | High                                  |

---

### Test Case 7: Calculate Portfolio Exposure  
| **Test Case ID** | TC_HIM_002                             |
|-------------------|---------------------------------------|
| **Description**   | Validate that portfolio exposure is calculated correctly. |
| **Precondition**  | Fund has valid holding data.          |
| **Test Steps**    | 1. Select a fund.<br>2. Navigate to the "Portfolio Exposure" page.<br>3. Verify the displayed exposures. |
| **Expected Result** | Portfolio exposures match the calculated values. |
| **Priority**      | Medium                                |

---

## **4. Document Management**

### Test Case 8: Upload Fund Documents  
| **Test Case ID** | TC_DM_001                              |
|-------------------|---------------------------------------|
| **Description**   | Verify that documents can be uploaded and retrieved. |
| **Precondition**  | User has access to the document repository. |
| **Test Steps**    | 1. Navigate to the "Upload Document" page.<br>2. Select a document file.<br>3. Click "Upload." |
| **Expected Result** | Document is uploaded and appears in the repository. |
| **Priority**      | Medium                                |

---

### Test Case 9: Version Control for Documents  
| **Test Case ID** | TC_DM_002                              |
|-------------------|---------------------------------------|
| **Description**   | Verify version control functionality for documents. |
| **Precondition**  | Document exists in the repository.    |
| **Test Steps**    | 1. Upload a new version of an existing document.<br>2. Verify the version history. |
| **Expected Result** | The new version is saved, and the history displays both versions. |
| **Priority**      | High                                  |

---

## **5. Investor Education**

### Test Case 10: Access Educational Content  
| **Test Case ID** | TC_IE_001                              |
|-------------------|---------------------------------------|
| **Description**   | Verify that educational content is accessible. |
| **Precondition**  | User is logged in.                   |
| **Test Steps**    | 1. Navigate to the "Investor Education" section.<br>2. Select a resource (e.g., article or video). |
| **Expected Result** | The resource loads successfully.   |
| **Priority**      | Low                                  |

---
