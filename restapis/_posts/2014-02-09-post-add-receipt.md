---
category: Receipt
path: '/api/addReceipt'
title: 'Add receipt'
type: 'POST'

layout: nil
---

## addReceipt Method

### Overview

> This method will be used for adding a receipt detail and attachment.

### Business Rule

* Fields (import details, attachments) under request must be mandatory.
* On the response, status after saving will be displayed.

### Usage

* This will be used on adding a receipt detail and attachment.

### Request

#### Import Details

<table>
	<tr>
		<th>Field Name</th>
		<th>Data Type</th>
		<th>Description</th>
		<th>Mandatory</th>
	</tr>
	<tr>
		<td>AgencyID</td>
		<td>string</td>
		<td>Agency ID</td>
		<td>yes</td>
	</tr>
	<tr>
		<td>WebBusinessID</td>
		<td>integer</td>
		<td>Landlord Web Business ID</td>
		<td>yes</td>
	</tr>
	<tr>
		<td>Account ID</td>
		<td>integer</td>
		<td>Landlord Account ID</td>
		<td>yes</td>
	</tr>
	<tr>
		<td>Action</td>
		<td>string</td>
		<td>Web Service Action</td>
		<td>yes</td>
	</tr>
	<tr>
		<td>PropertyID</td>
		<td>integer</td>
		<td>Property ID</td>
		<td>no</td>
	</tr>
	<tr>
		<td>ActionType</td>
		<td>string</td>
		<td>Web Service Action Type</td>
		<td>yes</td>
	</tr>
	<tr>
		<td>WebID</td>
		<td>integer</td>
		<td>Transaction ID</td>
		<td>yes</td>
	</tr>
	<tr>
		<td>RemoveWebID</td>
		<td>integer</td>
		<td>Transaction ID to be removed</td>
		<td>no</td>
	</tr>
	<tr>
		<td>ManagementBusinessID</td>
		<td>integer</td>
		<td>Management Business ID</td>
		<td>yes</td>
	</tr>
	<tr>
		<td>ReceiptNumber</td>
		<td>string</td>
		<td>Receipt Number</td>
		<td>yes</td>
	</tr>
	<tr>
		<td>ReceiptAmount</td>
		<td>double</td>
		<td>Receipt Amount</td>
		<td>yes</td>
	</tr>
	<tr>
		<td>ReceiptDebtorNoticeDate</td>
		<td>date</td>
		<td>Receipt Debtor Notice Date</td>
		<td>yes</td>
	</tr>	
	<tr>
		<td>MeetingID</td>
		<td>integer</td>
		<td>Meeting ID</td>
		<td>no</td>
	</tr>
	<tr>
		<td>CommonID</td>
		<td>integer</td>
		<td>Common ID</td>
		<td>yes</td>
	</tr>
	<tr>
		<td>DebtorRunID</td>
		<td>integer</td>
		<td>Debtor Run ID</td>
		<td>no</td>
	</tr>
	<tr>
		<td>DebtorAmountDue</td>
		<td>double</td>
		<td>Debtor Amount Due</td>
		<td>no</td>
	</tr>
	<tr>
		<td>ImageOrderNumber</td>
		<td>integer</td>
		<td>Image Order Number</td>
		<td>no</td>
	</tr>
</table>

### Attachments

<table>
	<tr>
		<th>Field Name</th>
		<th>Data Type</th>
		<th>Description</th>
		<th>Mandatory</th>
	</tr>
	<tr>
		<td>Filename</td>
		<td>string</td>
		<td>Filename ID</td>
		<td>yes</td>
	</tr>
	<tr>
		<td>InlineAttachment</td>
		<td>string</td>
		<td>InlineAttachment</td>
		<td>yes</td>
	</tr>
</table>

### Response

<table>
	<tr>
		<th>Field Name</th>
		<th>Data Type</th>
		<th>Description</th>
	</tr>
	<tr>
		<td>status</td>
		<td>string</td>
		<td>Status</td>
	</tr>
</table>

### Sample Request

#### Receipt

##### With Attachment
```
{
    "Transaction": {
        "Import": {
            "Details": {
                "AgencyID": "vtest123",
                "WebBusinessID": "25",
                "AccountID": "1135",
                "Action": "Receipt",
                "PropertyID": "0",
                "ActionType": "Add",
                "WebID": "16",
                "RemoveWebID": "0",
                "ManagementBusinessID": "19",
                "ReceiptNumber": "11",
                "ReceiptAmount": "389.76",
                "ReceiptDebtorNoticeDate": "28/10/2013",
                "MeetingID": "0",
                "CommonID": "14",
                "DebtorRunID": "0",
                "DebtorAmountDue": "0.00",
                "ImageOrderNumber": "00"
            }
        },
        "CompanyDetails": {
            "Company": {
                "ID": "vtest123",
                "Name": "Lorem ipsum dolor sit amet, consectetur",
                "ContactID": "1",
                "Contact": "Lorem ipsum dolor sit amet, consectetur",
                "Address1": "Lorem ipsum dolor sit amet, consectetur",
                "Address2": "Lorem ipsum dolor sit amet, consectetur",
                "BusinessNumber": "1234567890",
                "FaxNumber": "1234567890",
                "eMail": "test@sample.com",
                "URL": "www.google.com",
                "Street": "Lorem ipsum dolor sit amet, consectetur",
                "Suburb": "NEWPORT",
                "State": "VIC",
                "Postcode": "3150",
                "Country": "Australia"
            }
        },
        "Accounts": {
            "Account": [
                {
                    "Account": {
                        "ID": "1135",
                        "Owner": "Lorem ipsum dolor sit amet, consectetur",
                        "Address": "Lorem ipsum dolor sit amet, consectetur",
                        "BalanceHeld": "614.82",
                        "TotalInvoicesOutstanding": "0.00",
                        "AvailableFunds": "614.82",
                        "AvailableFundsasat": "29/10/2013"
                    }
                }
            ]
        },
        "Owners": {
            "Owner": [
                {
                    "Owner": {
                        "ID": "43",
                        "Name": "Lorem ipsum dolor sit amet, consectetur",
                        "Contact": "Lorem ipsum dolor sit amet, consectetur",
                        "Address1": "Lorem ipsum dolor sit amet, consectetur",
                        "Address2": "Lorem ipsum dolor sit amet, consectetur",
                        "eMail": "test@sample.com",
                        "UnitNo": "3",
                        "StreetNo": "9",
                        "Street": "Lorem ipsum dolor sit amet, consectetur",
                        "Suburb": "NEWPORT",
                        "State": "VIC",
                        "Postcode": "3015",
                        "Country": "Australia"
                    }
                },
                {
                    "Owner": {
                        "ID": "40",
                        "Name": "Lorem ipsum dolor sit amet, consectetur",
                        "Contact": "Lorem ipsum dolor sit amet, consectetur",
                        "Address1": "Lorem ipsum dolor sit amet, consectetur",
                        "Address2": "Lorem ipsum dolor sit amet, consectetur",
                        "eMail": "test@gmail.com",
                        "UnitNo": "3",
                        "StreetNo": "9",
                        "Street": "Basil Street",
                        "Suburb": "NEWPORT",
                        "State": "VIC",
                        "Postcode": "3015",
                        "Country": "Australia"
                    }
                },
                {
                    "Owner": {
                        "ID": "41",
                        "Name": "Lorem ipsum dolor sit amet, consectetur",
                        "Contact": "Lorem ipsum dolor sit amet, consectetur",
                        "Address1": "Lorem ipsum dolor sit amet, consectetur",
                        "Address2": "Lorem ipsum dolor sit amet, consectetur",
                        "eMail": "test@gmail.com",
                        "UnitNo": "2",
                        "StreetNo": "9",
                        "Street": "Basil Street",
                        "Suburb": "NEWPORT",
                        "State": "VIC",
                        "Postcode": "3015",
                        "Country": "Australia"
                    }
                }
            ]
        },
        "Properties": {
            "Property": [
                {
                    "Property": {
                        "ID": "36",
                        "Address": "Lorem ipsum dolor sit amet, consectetur",
                        "Address1": "Lorem ipsum dolor sit amet, consectetur",
                        "Address2": "Lorem ipsum dolor sit amet, consectetur",
                        "Bedrooms": "0",
                        "Bathrooms": "0",
                        "CarSpaces": "0",
                        "StreetNo": "9",
                        "Street": "Basil Street",
                        "Suburb": "NEWPORT",
                        "State": "VIC",
                        "Postcode": "3015",
                        "Country": "Australia"
                    }
                },
                {
                    "Property": {
                        "ID": "39",
                        "Address": "Lorem ipsum dolor sit amet, consectetur",
                        "Address1": "Lorem ipsum dolor sit amet, consectetur",
                        "Address2": "Lorem ipsum dolor sit amet, consectetur",
                        "Bedrooms": "0",
                        "Bathrooms": "0",
                        "CarSpaces": "0",
                        "UnitNo": "3",
                        "StreetNo": "9",
                        "Street": "Basil Street",
                        "Suburb": "NEWPORT",
                        "State": "VIC",
                        "Postcode": "3015",
                        "Country": "Australia"
                    }
                },
                {
                    "Property": {
                        "ID": "37",
                        "Address": "Lorem ipsum dolor sit amet, consectetur",
                        "Address1": "Lorem ipsum dolor sit amet, consectetur",
                        "Address2": "Lorem ipsum dolor sit amet, consectetur",
                        "Bedrooms": "0",
                        "Bathrooms": "0",
                        "CarSpaces": "0",
                        "UnitNo": "3",
                        "StreetNo": "9",
                        "Street": "Basil Street",
                        "Suburb": "NEWPORT",
                        "State": "VIC",
                        "Postcode": "3015",
                        "Country": "Australia"
                    }
                },
                {
                    "Property": {
                        "ID": "38",
                        "Address": "Lorem ipsum dolor sit amet, consectetur",
                        "Address1": "Lorem ipsum dolor sit amet, consectetur",
                        "Address2": "Lorem ipsum dolor sit amet, consectetur",
                        "Bedrooms": "0",
                        "Bathrooms": "0",
                        "CarSpaces": "0",
                        "UnitNo": "2",
                        "StreetNo": "9",
                        "Street": "Basil Street",
                        "Suburb": "NEWPORT",
                        "State": "VIC",
                        "Postcode": "3015",
                        "Country": "Australia"
                    }
                }
            ],
            "CommonProperty": {
                "Business": {
                    "ID": "14",
                    "AccountID": "1135",
                    "PropertyID": "36",
                    "ManagerID": "9",
                    "Address": "Lorem ipsum dolor sit amet, consectetur",
                    "StrataNumber": "Lorem ipsum dolor sit amet, consectetur",
                    "NextAGM": "02/10/2013",
                    "StartFinancialYear": "01/09/2013",
                    "EndFinancialYear": "31/08/2014",
                    "NextMeetingDate": "02/10/2013",
                    "NextMeetingTime": "5:00 PM",
                    "NextMeetingType": "Lorem ipsum dolor sit amet, consectetur",
                    "NextMeetingBuilding": "Lorem ipsum dolor sit amet, consectetur",
                    "NextMeetingAddress": "Lorem ipsum dolor sit amet, consectetur",
                    "NextMeetingSuburb": "Lorem ipsum dolor sit amet, consectetur"
                }
            },
            "Strata": [
                {
                    "Business": {
                        "ID": "17",
                        "AccountID": "1135",
                        "PropertyID": "37",
                        "ManagerID": "9",
                        "Address": "Lorem ipsum dolor sit amet, consectetur",
                        "Member": "Lorem ipsum dolor sit amet, consectetur",
                        "Fee": "354.33",
                        "Period": "Q",
                        "PaidTo": "01/09/2013",
                        "Credit": "0",
                        "LiabilityUnits": "100",
                        "EntitlementUnits": "105",
                        "LotNo": "1",
                        "FeeOutstanding": "0",
                        "OtherChargesOutstanding": "0",
                        "TotalOutstanding": "0",
                        "Manager": "Lorem ipsum dolor sit amet, consectetur",
                        "ManagerMobile": "0413 012 213",
                        "ManagerBusiness": "03-9982-1301",
                        "Manageremail": "test@sample.com",
                        "Committee": "N"
                    }
                },
                {
                    "Business": {
                        "ID": "19",
                        "AccountID": "1135",
                        "PropertyID": "38",
                        "ManagerID": "9",
                        "Address": "Lorem ipsum dolor sit amet, consectetur",
                        "Member": "Lorem ipsum dolor sit amet, consectetur",
                        "Fee": "354.33",
                        "Period": "Q",
                        "PaidTo": "30/11/2013",
                        "Credit": "0",
                        "LiabilityUnits": "100",
                        "EntitlementUnits": "90",
                        "LotNo": "2",
                        "FeeOutstanding": "0",
                        "OtherChargesOutstanding": "0",
                        "TotalOutstanding": "0",
                        "Manager": "Lorem ipsum dolor sit amet, consectetur",
                        "ManagerMobile": "0413 012 213",
                        "ManagerBusiness": "03-9982-1301",
                        "Manageremail": "test@sample.com",
                        "Committee": "N"
                    }
                },
                {
                    "Business": {
                        "ID": "21",
                        "AccountID": "1135",
                        "PropertyID": "39",
                        "ManagerID": "9",
                        "Address": "Lorem ipsum dolor sit amet, consectetur",
                        "Member": "Lorem ipsum dolor sit amet, consectetur",
                        "Fee": "354.34",
                        "Period": "Q",
                        "PaidTo": "01/09/2013",
                        "Credit": "0",
                        "LiabilityUnits": "100",
                        "EntitlementUnits": "105",
                        "LotNo": "3",
                        "FeeOutstanding": "354.34",
                        "OtherChargesOutstanding": "35.43",
                        "TotalOutstanding": "389.77",
                        "Manager": "Lorem ipsum dolor sit amet, consectetur",
                        "ManagerMobile": "1234567890",
                        "ManagerBusiness": "1234567890",
                        "Manageremail": "test@sample.com",
                        "Committee": "N"
                    }
                }
            ],
            "Contacts": [
                {
                    "Contact": {
                        "Relation": "Branch",
                        "ContactID": "1",
                        "IsCompany": "Y",
                        "FirstName": "Lorem ipsum dolor sit amet, consectetur",
                        "LastName": "Lorem ipsum dolor sit amet, consectetur",
                        "FullName": "Lorem ipsum dolor sit amet, consectetur",
                        "Mobile": "1234567890",
                        "eMail": "test@sample.com",
                        "BusinessID": "17",
                        "AccountID": "1135"
                    }
                },
                {
                    "Contact": {
                        "Relation": "Branch",
                        "ContactID": "1",
                        "IsCompany": "Y",
                        "FirstName": "Lorem ipsum dolor sit amet, consectetur",
                        "LastName": "Lorem ipsum dolor sit amet, consectetur",
                        "FullName": "Lorem ipsum dolor sit amet, consectetur",
                        "Mobile": "1234567890",
                        "eMail": "test@sample.com",
                        "BusinessID": "19",
                        "AccountID": "1135"
                    }
                },
                {
                    "Contact": {
                        "Relation": "Branch",
                        "ContactID": "1",
                        "IsCompany": "Y",
                        "FirstName": "Lorem ipsum dolor sit amet, consectetur",
                        "LastName": "Lorem ipsum dolor sit amet, consectetur",
                        "FullName": "Lorem ipsum dolor sit amet, consectetur",
                        "Mobile": "0418 316-554",
                        "eMail": "test@sample.com",
                        "BusinessID": "21",
                        "AccountID": "1135"
                    }
                },
                {
                    "Contact": {
                        "Relation": "Correspondence",
                        "ContactID": "40",
                        "IsCompany": "N",
                        "FirstName": "Lorem ipsum dolor sit amet, consectetur",
                        "LastName": "Lorem ipsum dolor sit amet, consectetur",
                        "FullName": "Lorem ipsum dolor sit amet, consectetur",
                        "Mobile": "1234567890",
                        "eMail": "test@sample.com",
                        "BusinessID": "17",
                        "AccountID": "1135"
                    }
                },
                {
                    "Contact": {
                        "Relation": "Correspondence",
                        "ContactID": "41",
                        "IsCompany": "N",
                        "FirstName": "Lorem ipsum dolor sit amet, consectetur",
                        "LastName": "Lorem ipsum dolor sit amet, consectetur",
                        "FullName": "Lorem ipsum dolor sit amet, consectetur",
                        "eMail": "test@sample.com",
                        "BusinessID": "19",
                        "AccountID": "1135"
                    }
                },
                {
                    "Contact": {
                        "Relation": "Correspondence",
                        "ContactID": "43",
                        "IsCompany": "N",
                        "FirstName": "Lorem ipsum dolor sit amet, consectetur",
                        "LastName": "Lorem ipsum dolor sit amet, consectetur",
                        "FullName": "Lorem ipsum dolor sit amet, consectetur",
                        "Mobile": "1234567890",
                        "eMail": "test@sample.com",
                        "BusinessID": "21",
                        "AccountID": "1135"
                    }
                },
                {
                    "Contact": {
                        "Relation": "Manager",
                        "ContactID": "9",
                        "IsCompany": "N",
                        "FirstName": "Lorem ipsum dolor sit amet, consectetur",
                        "LastName": "Lorem ipsum dolor sit amet, consectetur",
                        "FullName": "Lorem ipsum dolor sit amet, consectetur",
                        "Mobile": "1234567890",
                        "eMail": "test@sample.com",
                        "BusinessID": "17",
                        "AccountID": "1135"
                    }
                },
                {
                    "Contact": {
                        "Relation": "Manager",
                        "ContactID": "9",
                        "IsCompany": "N",
                        "FirstName": "Lorem ipsum dolor sit amet, consectetur",
                        "LastName": "Lorem ipsum dolor sit amet, consectetur",
                        "FullName": "Lorem ipsum dolor sit amet, consectetur",
                        "Mobile": "1234567890",
                        "eMail": "test@sample.com",
                        "BusinessID": "19",
                        "AccountID": "1135"
                    }
                },
                {
                    "Contact": {
                        "Relation": "Manager",
                        "ContactID": "9",
                        "IsCompany": "N",
                        "FirstName": "Lorem ipsum dolor sit amet, consectetur",
                        "LastName": "Lorem ipsum dolor sit amet, consectetur",
                        "FullName": "Lorem ipsum dolor sit amet, consectetur",
                        "Mobile": "1234567890",
                        "eMail": "test@sample.com",
                        "BusinessID": "21",
                        "AccountID": "1135"
                    }
                },
                {
                    "Contact": {
                        "Relation": "Member",
                        "ContactID": "40",
                        "IsCompany": "N",
                        "FirstName": "Lorem ipsum dolor sit amet, consectetur",
                        "LastName": "Lorem ipsum dolor sit amet, consectetur",
                        "FullName": "Lorem ipsum dolor sit amet, consectetur",
                        "Mobile": "1234567890",
                        "eMail": "test@sample.com",
                        "BusinessID": "17",
                        "AccountID": "1135"
                    }
                },
                {
                    "Contact": {
                        "Relation": "Member",
                        "ContactID": "41",
                        "IsCompany": "N",
                        "FirstName": "Lorem ipsum dolor sit amet, consectetur",
                        "LastName": "Lorem ipsum dolor sit amet, consectetur",
                        "FullName": "Lorem ipsum dolor sit amet, consectetur",
                        "eMail": "test@sample.com",
                        "BusinessID": "19",
                        "AccountID": "1135"
                    }
                },
                {
                    "Contact": {
                        "Relation": "Member",
                        "ContactID": "43",
                        "IsCompany": "N",
                        "FirstName": "Lorem ipsum dolor sit amet, consectetur",
                        "LastName": "Lorem ipsum dolor sit amet, consectetur",
                        "FullName": "Lorem ipsum dolor sit amet, consectetur",
                        "Mobile": "1234567890",
                        "eMail": "test@sample.com",
                        "BusinessID": "21",
                        "AccountID": "1135"
                    }
                },
                {
                    "Contact": {
                        "Relation": "OCSP:",
                        "ContactID": "38",
                        "IsCompany": "Y",
                        "LastName": "Lorem ipsum dolor sit amet, consectetur",
                        "FullName": "Lorem ipsum dolor sit amet, consectetur",
                        "eMail": "test@sample.com",
                        "BusinessID": "17",
                        "AccountID": "1135"
                    }
                },
                {
                    "Contact": {
                        "Relation": "OCSP:",
                        "ContactID": "38",
                        "IsCompany": "Y",
                        "LastName": "Lorem ipsum dolor sit amet, consectetur",
                        "FullName": "Lorem ipsum dolor sit amet, consectetur",
                        "eMail": "test@sample.com",
                        "BusinessID": "19",
                        "AccountID": "1135"
                    }
                },
                {
                    "Contact": {
                        "Relation": "OCSP:",
                        "ContactID": "38",
                        "IsCompany": "Y",
                        "LastName": "Lorem ipsum dolor sit amet, consectetur",
                        "FullName": "Lorem ipsum dolor sit amet, consectetur",
                        "eMail": "test@sample.com",
                        "BusinessID": "21",
                        "AccountID": "1135"
                    }
                },
                {
                    "Contact": {
                        "Relation": "PaymentFrom",
                        "ContactID": "40",
                        "IsCompany": "N",
                        "FirstName": "Anne",
                        "LastName": "Han Le",
                        "FullName": "Anne Han Le",
                        "Mobile": "0413 151-201",
                        "eMail": "test@sample.com",
                        "BusinessID": "17",
                        "AccountID": "1135"
                    }
                },
                {
                    "Contact": {
                        "Relation": "PaymentFrom",
                        "ContactID": "41",
                        "IsCompany": "N",
                        "FirstName": "Lorem ipsum dolor sit amet, consectetur",
                        "LastName": "Lorem ipsum dolor sit amet, consectetur",
                        "FullName": "Lorem ipsum dolor sit amet, consectetur",
                        "eMail": "test@sample.com",
                        "BusinessID": "19",
                        "AccountID": "1135"
                    }
                },
                {
                    "Contact": {
                        "Relation": "PaymentFrom",
                        "ContactID": "43",
                        "IsCompany": "N",
                        "FirstName": "Lorem ipsum dolor sit amet, consectetur",
                        "LastName": "Lorem ipsum dolor sit amet, consectetur",
                        "FullName": "Lorem ipsum dolor sit amet, consectetur",
                        "Mobile": "0411 733 198",
                        "eMail": "test@sample.com",
                        "BusinessID": "21",
                        "AccountID": "1135"
                    }
                },
                {
                    "Contact": {
                        "Relation": "Account Owner",
                        "ContactID": "38",
                        "IsCompany": "Y",
                        "LastName": "Lorem ipsum dolor sit amet, consectetur",
                        "FullName": "Lorem ipsum dolor sit amet, consectetur",
                        "eMail": "test@sample.com",
                        "BusinessID": "0",
                        "AccountID": "1135"
                    }
                }
            ],
            "Insurance": {
                "Business": {
                    "ID": "15",
                    "AccountID": "1135",
                    "PropertyID": "36",
                    "Address": "Lorem ipsum dolor sit amet, consectetur",
                    "Supplier": "Lorem ipsum dolor sit amet, consectetur",
                    "RenewalDate": "06/09/2013",
                    "PolicyName": "Lorem ipsum dolor sit amet, consectetur",
                    "PolicyNumber": "123456890",
                    "BuildingAmount": "897000",
                    "PublicLiability": "10000000",
                    "Premium": "1368.95",
                    "Excess": "100",
                    "VoluntaryWorkers": "250000"
                }
            },
            "Attachments": {
                "Attachment": [
                    {
                        "Attachment": {
                            "Filename": "68-01-11-2013-55844.PDF",
                            "InlineAttachment": "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YmoNCjcgMCBvYmoNCjEyNjUNCmVuZG9iag0KOCAwIG9iag0KWyAvUERGIC9UZXh0IC9JbWFnZUMgXSANCmVuZG9iag0KMTEgMCBvYmoNCjw8IC9UeXBlIC9Gb250IA0KL05hbWUgL0YwIA0KL0Jhc2VGb250IC9Db3VyaWVyTmV3IA0KL0VuY29kaW5nIDIwIDAgUg0KL1N1YnR5cGUgL1RydWVUeXBlIA0KL0ZpcnN0Q2hhciAzMA0KL0xhc3RDaGFyIDI1NQ0KL1dpZHRocyBbDQo2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCANCjYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIA0KNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgDQo2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCANCjYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDAgNjAwIDYwMCA2MDAgNjAwIDYwMCANCjYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDAgNjAwIDAgMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgMCA2MDAgNjAwIDYwMCA2MDAgMCANCjYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIA0KNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgDQo2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCANCjYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIA0KNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCANCl0NCi9Gb250RGVzY3JpcHRvciAyMSAwIFIgDQo+Pg0KZW5kb2JqDQoyMCAwIG9iag0KPDwgL1R5cGUgL0VuY29kaW5nIA0KL0Jhc2VFbmNvZGluZyAvV2luQW5zaUVuY29kaW5nIA0KPj4NCmVuZG9iag0KMjEgMCBvYmoNCjw8IC9UeXBlIC9Gb250RGVzY3JpcHRvciANCi9Gb250TmFtZSAvQ291cmllck5ldw0KL0ZvbnRCQm94IFsgMCAwIDAgMCBdIA0KL0ZsYWdzIDM0DQovU3RlbVYgODQNCi9JdGFsaWNBbmdsZSAwDQovQ2FwSGVpZ2h0IDEwMDANCi9Bc2NlbnQgMTAwMA0KL0Rlc2NlbnQgLTI1MA0KL01heFdpZHRoIDEwMDANCj4+DQplbmRvYmoNCjEyIDAgb2JqDQo8PCAvVHlwZSAvRm9udCANCi9OYW1lIC9GMSANCi9CYXNlRm9udCAvQ291cmllck5ldyxCb2xkIA0KL0VuY29kaW5nIDIyIDAgUg0KL1N1YnR5cGUgL1RydWVUeXBlIA0KL0ZpcnN0Q2hhciAzMA0KL0xhc3RDaGFyIDI1NQ0KL1dpZHRocyBbDQo2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCANCjYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIA0KNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgDQo2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCANCjYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDAgNjAwIDYwMCA2MDAgNjAwIDYwMCANCjYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDAgNjAwIDAgMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgMCA2MDAgNjAwIDYwMCA2MDAgMCANCjYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIA0KNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgDQo2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCANCjYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIA0KNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCANCl0NCi9Gb250RGVzY3JpcHRvciAyMyAwIFIgDQo+Pg0KZW5kb2JqDQoyMiAwIG9iag0KPDwgL1R5cGUgL0VuY29kaW5nIA0KL0Jhc2VFbmNvZGluZyAvV2luQW5zaUVuY29kaW5nIA0KPj4NCmVuZG9iag0KMjMgMCBvYmoNCjw8IC9UeXBlIC9Gb250RGVzY3JpcHRvciANCi9Gb250TmFtZSAvQ291cmllck5ldyxCb2xkDQovRm9udEJCb3ggWyAwIDAgMCAwIF0gDQovRmxhZ3MgMzQNCi9TdGVtViA4NA0KL0l0YWxpY0FuZ2xlIDANCi9DYXBIZWlnaHQgMTAwMA0KL0FzY2VudCAxMDAwDQovRGVzY2VudCAtMjUwDQovTWF4V2lkdGggMTAwMA0KPj4NCmVuZG9iag0KMTMgMCBvYmoNCjw8IC9UeXBlIC9Gb250IA0KL05hbWUgL0YyIA0KL0Jhc2VGb250IC9Db3VyaWVyTmV3LEl0YWxpYyANCi9FbmNvZGluZyAyNCAwIFINCi9TdWJ0eXBlIC9UcnVlVHlwZSANCi9GaXJzdENoYXIgMzANCi9MYXN0Q2hhciAyNTUNCi9XaWR0aHMgWw0KNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgDQo2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCANCjYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIA0KNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgDQo2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgDQo2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCAwIDYwMCAwIDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDAgNjAwIDYwMCA2MDAgNjAwIDAgDQo2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCANCjYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIA0KNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgDQo2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCANCjYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgNjAwIDYwMCA2MDAgDQpdDQovRm9udERlc2NyaXB0b3IgMjUgMCBSIA0KPj4NCmVuZG9iag0KMjQgMCBvYmoNCjw8IC9UeXBlIC9FbmNvZGluZyANCi9CYXNlRW5jb2RpbmcgL1dpbkFuc2lFbmNvZGluZyANCj4+DQplbmRvYmoNCjI1IDAgb2JqDQo8PCAvVHlwZSAvRm9udERlc2NyaXB0b3IgDQovRm9udE5hbWUgL0NvdXJpZXJOZXcsSXRhbGljDQovRm9udEJCb3ggWyAwIDAgMCAwIF0gDQovRmxhZ3MgOTgNCi9TdGVtViA4NA0KL0l0YWxpY0FuZ2xlIDANCi9DYXBIZWlnaHQgMTAwMA0KL0FzY2VudCAxMDAwDQovRGVzY2VudCAtMjUwDQovTWF4V2lkdGggMTAwMA0KPj4NCmVuZG9iag0KMTQgMCBvYmoNCjw8IC9UeXBlIC9Gb250IA0KL05hbWUgL0YzIA0KL0Jhc2VGb250IC9BcmlhbCANCi9FbmNvZGluZyAyNiAwIFINCi9TdWJ0eXBlIC9UcnVlVHlwZSANCi9GaXJzdENoYXIgMzANCi9MYXN0Q2hhciAyNTUNCi9XaWR0aHMgWw0KNzUwIDc1MCAyNzggMjc4IDM1NSA1NTYgNTU2IDg4OSA2NjcgMTkxIDMzMyAzMzMgMzg5IDU4NCAyNzggMzMzIDI3OCAyNzggNTU2IDU1NiA1NTYgDQo1NTYgNTU2IDU1NiA1NTYgNTU2IDU1NiA1NTYgMjc4IDI3OCA1ODQgNTg0IDU4NCA1NTYgMTAxNSA2NjcgNjY3IDcyMiA3MjIgNjY3IDYxMSANCjc3OCA3MjIgMjc4IDUwMCA2NjcgNTU2IDgzMyA3MjIgNzc4IDY2NyA3NzggNzIyIDY2NyA2MTEgNzIyIDY2NyA5NDQgNjY3IDY2NyA2MTEgMjc4IA0KMjc4IDI3OCA0NjkgNTU2IDMzMyA1NTYgNTU2IDUwMCA1NTYgNTU2IDI3OCA1NTYgNTU2IDIyMiAyMjIgNTAwIDIyMiA4MzMgNTU2IDU1NiA1NTYgDQo1NTYgMzMzIDUwMCAyNzggNTU2IDUwMCA3MjIgNTAwIDUwMCA1MDAgMzM0IDI2MCAzMzQgNTg0IDc1MCA1NTYgMCAyMjIgNTU2IDMzMyAxMDAwIA0KNTU2IDU1NiAzMzMgMTAwMCA2NjcgMzMzIDEwMDAgMCA2MTEgMCAwIDIyMiAyMjIgMzMzIDMzMyAzNTAgNTU2IDEwMDAgMzMzIDEwMDAgNTAwIA0KMzMzIDk0NCAwIDUwMCA2NjcgMjc4IDMzMyA1NTYgNTU2IDU1NiA1NTYgMjYwIDU1NiAzMzMgNzM3IDM3MCA1NTYgNTg0IDMzMyA3MzcgNTUyIA0KNDAwIDU0OSAzMzMgMzMzIDMzMyA1NzYgNTM3IDMzMyAzMzMgMzMzIDM2NSA1NTYgODM0IDgzNCA4MzQgNjExIDY2NyA2NjcgNjY3IDY2NyA2NjcgDQo2NjcgMTAwMCA3MjIgNjY3IDY2NyA2NjcgNjY3IDI3OCAyNzggMjc4IDI3OCA3MjIgNzIyIDc3OCA3NzggNzc4IDc3OCA3NzggNTg0IDc3OCANCjcyMiA3MjIgNzIyIDcyMiA2NjcgNjY3IDYxMSA1NTYgNTU2IDU1NiA1NTYgNTU2IDU1NiA4ODkgNTAwIDU1NiA1NTYgNTU2IDU1NiAyNzggMjc4IA0KMjc4IDI3OCA1NTYgNTU2IDU1NiA1NTYgNTU2IDU1NiA1NTYgNTQ5IDYxMSA1NTYgNTU2IDU1NiA1NTYgNTAwIDU1NiA1MDAgDQpdDQovRm9udERlc2NyaXB0b3IgMjcgMCBSIA0KPj4NCmVuZG9iag0KMjYgMCBvYmoNCjw8IC9UeXBlIC9FbmNvZGluZyANCi9CYXNlRW5jb2RpbmcgL1dpbkFuc2lFbmNvZGluZyANCj4+DQplbmRvYmoNCjI3IDAgb2JqDQo8PCAvVHlwZSAvRm9udERlc2NyaXB0b3IgDQovRm9udE5hbWUgL0FyaWFsDQovRm9udEJCb3ggWyAwIDAgMCAwIF0gDQovRmxhZ3MgMzINCi9TdGVtViA4NA0KL0l0YWxpY0FuZ2xlIDANCi9DYXBIZWlnaHQgMTAwMA0KL0FzY2VudCAxMDAwDQovRGVzY2VudCAtMjUwDQovTWF4V2lkdGggMTAwMA0KPj4NCmVuZG9iag0KMTUgMCBvYmoNCjw8IC9UeXBlIC9Gb250IA0KL05hbWUgL0Y0IA0KL0Jhc2VGb250IC9BcmlhbCxCb2xkIA0KL0VuY29kaW5nIDI4IDAgUg0KL1N1YnR5cGUgL1RydWVUeXBlIA0KL0ZpcnN0Q2hhciAzMA0KL0xhc3RDaGFyIDI1NQ0KL1dpZHRocyBbDQo3NTAgNzUwIDI3OCAzMzMgNDc0IDU1NiA1NTYgODg5IDcyMiAyMzggMzMzIDMzMyAzODkgNTg0IDI3OCAzMzMgMjc4IDI3OCA1NTYgNTU2IDU1NiANCjU1NiA1NTYgNTU2IDU1NiA1NTYgNTU2IDU1NiAzMzMgMzMzIDU4NCA1ODQgNTg0IDYxMSA5NzUgNzIyIDcyMiA3MjIgNzIyIDY2NyA2MTEgNzc4IA0KNzIyIDI3OCA1NTYgNzIyIDYxMSA4MzMgNzIyIDc3OCA2NjcgNzc4IDcyMiA2NjcgNjExIDcyMiA2NjcgOTQ0IDY2NyA2NjcgNjExIDMzMyAyNzggDQozMzMgNTg0IDU1NiAzMzMgNTU2IDYxMSA1NTYgNjExIDU1NiAzMzMgNjExIDYxMSAyNzggMjc4IDU1NiAyNzggODg5IDYxMSA2MTEgNjExIDYxMSANCjM4OSA1NTYgMzMzIDYxMSA1NTYgNzc4IDU1NiA1NTYgNTAwIDM4OSAyODAgMzg5IDU4NCA3NTAgNTU2IDAgMjc4IDU1NiA1MDAgMTAwMCA1NTYgDQo1NTYgMzMzIDEwMDAgNjY3IDMzMyAxMDAwIDAgNjExIDAgMCAyNzggMjc4IDUwMCA1MDAgMzUwIDU1NiAxMDAwIDMzMyAxMDAwIDU1NiAzMzMgDQo5NDQgMCA1MDAgNjY3IDI3OCAzMzMgNTU2IDU1NiA1NTYgNTU2IDI4MCA1NTYgMzMzIDczNyAzNzAgNTU2IDU4NCAzMzMgNzM3IDU1MiA0MDAgDQo1NDkgMzMzIDMzMyAzMzMgNTc2IDU1NiAzMzMgMzMzIDMzMyAzNjUgNTU2IDgzNCA4MzQgODM0IDYxMSA3MjIgNzIyIDcyMiA3MjIgNzIyIDcyMiANCjEwMDAgNzIyIDY2NyA2NjcgNjY3IDY2NyAyNzggMjc4IDI3OCAyNzggNzIyIDcyMiA3NzggNzc4IDc3OCA3NzggNzc4IDU4NCA3NzggNzIyIA0KNzIyIDcyMiA3MjIgNjY3IDY2NyA2MTEgNTU2IDU1NiA1NTYgNTU2IDU1NiA1NTYgODg5IDU1NiA1NTYgNTU2IDU1NiA1NTYgMjc4IDI3OCAyNzggDQoyNzggNjExIDYxMSA2MTEgNjExIDYxMSA2MTEgNjExIDU0OSA2MTEgNjExIDYxMSA2MTEgNjExIDU1NiA2MTEgNTU2IA0KXQ0KL0ZvbnREZXNjcmlwdG9yIDI5IDAgUiANCj4+DQplbmRvYmoNCjI4IDAgb2JqDQo8PCAvVHlwZSAvRW5jb2RpbmcgDQovQmFzZUVuY29kaW5nIC9XaW5BbnNpRW5jb2RpbmcgDQo+Pg0KZW5kb2JqDQoyOSAwIG9iag0KPDwgL1R5cGUgL0ZvbnREZXNjcmlwdG9yIA0KL0ZvbnROYW1lIC9BcmlhbCxCb2xkDQovRm9udEJCb3ggWyAwIDAgMCAwIF0gDQovRmxhZ3MgMzINCi9TdGVtViA4NA0KL0l0YWxpY0FuZ2xlIDANCi9DYXBIZWlnaHQgMTAwMA0KL0FzY2VudCAxMDAwDQovRGVzY2VudCAtMjUwDQovTWF4V2lkdGggMTAwMA0KPj4NCmVuZG9iag0KMiAwIG9iag0KPDwNCi9DcmVhdG9yIChURXh0cmFEZXZpY2VzKQ0KL0NyZWF0aW9uRGF0ZSAoRDoyMDEzMTEwMTA5MDA0NykNCi9UaXRsZSAoKQ0KL0F1dGhvciAoVEV4dHJhRGV2aWNlcykNCi9Qcm9kdWNlciAoVEV4dHJhRGV2aWNlcykNCi9LZXl3b3JkcyAoKQ0KL1N1YmplY3QgKCkNCj4+DQplbmRvYmoNCjMgMCBvYmoNCjw8IC9UeXBlIC9QYWdlcyANCi9LaWRzIFsgNCAwIFIgIF0gDQovQ291bnQgMSA+PiANCmVuZG9iag0KNCAwIG9iag0KPDwgL1R5cGUgL1BhZ2VzIA0KL0tpZHMgWyAgNSAwIFIgXSANCi9Db3VudCAxIA0KL1BhcmVudCAzIDAgUiA+PiANCmVuZG9iag0KeHJlZg0KMCAzMA0KMDAwMDAwMDAwMCA2NTUzNSBmDQowMDAwMDAwMDEwIDAwMDAwIG4NCjAwMDAwOTUxNDUgMDAwMDAgbg0KMDAwMDA5NTMyMCAwMDAwMCBuDQowMDAwMDk1Mzg4IDAwMDAwIG4NCjAwMDAwMDAwNjUgMDAwMDAgbg0KMDAwMDA4Njg1OSAwMDAwMCBuDQowMDAwMDg4MjA0IDAwMDAwIG4NCjAwMDAwODgyMjcgMDAwMDAgbg0KMDAwMDA4NjcwOCAwMDAwMCBuDQowMDAwMDg2NjgyIDAwMDAwIG4NCjAwMDAwODgyNjkgMDAwMDAgbg0KMDAwMDA4OTYzOCAwMDAwMCBuDQowMDAwMDkxMDE3IDAwMDAwIG4NCjAwMDAwOTI0MDAgMDAwMDAgbg0KMDAwMDA5Mzc2OCAwMDAwMCBuDQowMDAwMDAwMTk2IDAwMDAwIG4NCjAwMDAwNDMzNTUgMDAwMDAgbg0KMDAwMDA0MzM4MCAwMDAwMCBuDQowMDAwMDg2NjU3IDAwMDAwIG4NCjAwMDAwODkzNjYgMDAwMDAgbg0KMDAwMDA4OTQ0MiAwMDAwMCBuDQowMDAwMDkwNzQwIDAwMDAwIG4NCjAwMDAwOTA4MTYgMDAwMDAgbg0KMDAwMDA5MjEyMSAwMDAwMCBuDQowMDAwMDkyMTk3IDAwMDAwIG4NCjAwMDAwOTM1MDEgMDAwMDAgbg0KMDAwMDA5MzU3NyAwMDAwMCBuDQowMDAwMDk0ODczIDAwMDAwIG4NCjAwMDAwOTQ5NDkgMDAwMDAgbg0KdHJhaWxlcg0KPDwgL1Jvb3QgMSAwIFIgDQovSUQgWzw+PD5dIA0KL0luZm8gMiAwIFIgDQovU2l6ZSAzMCA+PiANCnN0YXJ0eHJlZg0KOTU0NzINCiUlRU9G"
                        }
                    }
                ]
            }
        }
    }
}
```

##### Without Attachment
```
{
   "Transaction":{
      "Import":{
         "Details":{
            "AgencyID":"vtest123",
            "WebBusinessID":"25",
            "AccountID":"1135",
            "Action":"Receipt",
            "PropertyID":"0",
            "ActionType":"Add",
            "WebID":"16",
            "RemoveWebID":"0",
            "ManagementBusinessID":"19",
            "ReceiptNumber":"11",
            "ReceiptAmount":"389.76",
            "ReceiptDebtorNoticeDate":"28/10/2013",
            "MeetingID":"0",
            "CommonID":"14",
            "DebtorRunID":"0",
            "DebtorAmountDue":"0.00",
            "ImageOrderNumber":"00"
         }
      },
      "CompanyDetails":{
         "Company":{
            "ID":"vtest123",
            "Name":"Lorem ipsum dolor sit amet, consectetur",
            "ContactID":"1",
            "Contact":"Lorem ipsum dolor sit amet, consectetur",
            "Address1":"Lorem ipsum dolor sit amet, consectetur",
            "Address2":"Lorem ipsum dolor sit amet, consectetur",
            "BusinessNumber":"1234567890",
            "FaxNumber":"1234567890",
            "eMail":"test@sample.com",
            "URL":"www.google.com",
            "Street":"Lorem ipsum dolor sit amet, consectetur",
            "Suburb":"NEWPORT",
            "State":"VIC",
            "Postcode":"3150",
            "Country":"Australia"
         }
      },
      "Accounts":{
         "Account":[
            {
               "Account":{
                  "ID":"1135",
                  "Owner":"Lorem ipsum dolor sit amet, consectetur",
                  "Address":"Lorem ipsum dolor sit amet, consectetur",
                  "BalanceHeld":"614.82",
                  "TotalInvoicesOutstanding":"0.00",
                  "AvailableFunds":"614.82",
                  "AvailableFundsasat":"29/10/2013"
               }
            }
         ]
      },
      "Owners":{
         "Owner":[
            {
               "Owner":{
                  "ID":"43",
                  "Name":"Lorem ipsum dolor sit amet, consectetur",
                  "Contact":"Lorem ipsum dolor sit amet, consectetur",
                  "Address1":"Lorem ipsum dolor sit amet, consectetur",
                  "Address2":"Lorem ipsum dolor sit amet, consectetur",
                  "eMail":"test@sample.com",
                  "UnitNo":"3",
                  "StreetNo":"9",
                  "Street":"Lorem ipsum dolor sit amet, consectetur",
                  "Suburb":"NEWPORT",
                  "State":"VIC",
                  "Postcode":"3015",
                  "Country":"Australia"
               }
            },
            {
               "Owner":{
                  "ID":"40",
                  "Name":"Lorem ipsum dolor sit amet, consectetur",
                  "Contact":"Lorem ipsum dolor sit amet, consectetur",
                  "Address1":"Lorem ipsum dolor sit amet, consectetur",
                  "Address2":"Lorem ipsum dolor sit amet, consectetur",
                  "eMail":"test@gmail.com",
                  "UnitNo":"3",
                  "StreetNo":"9",
                  "Street":"Basil Street",
                  "Suburb":"NEWPORT",
                  "State":"VIC",
                  "Postcode":"3015",
                  "Country":"Australia"
               }
            },
            {
               "Owner":{
                  "ID":"41",
                  "Name":"Lorem ipsum dolor sit amet, consectetur",
                  "Contact":"Lorem ipsum dolor sit amet, consectetur",
                  "Address1":"Lorem ipsum dolor sit amet, consectetur",
                  "Address2":"Lorem ipsum dolor sit amet, consectetur",
                  "eMail":"test@gmail.com",
                  "UnitNo":"2",
                  "StreetNo":"9",
                  "Street":"Basil Street",
                  "Suburb":"NEWPORT",
                  "State":"VIC",
                  "Postcode":"3015",
                  "Country":"Australia"
               }
            }
         ]
      },
      "Properties":{
         "Property":[
            {
               "Property":{
                  "ID":"36",
                  "Address":"Lorem ipsum dolor sit amet, consectetur",
                  "Address1":"Lorem ipsum dolor sit amet, consectetur",
                  "Address2":"Lorem ipsum dolor sit amet, consectetur",
                  "Bedrooms":"0",
                  "Bathrooms":"0",
                  "CarSpaces":"0",
                  "StreetNo":"9",
                  "Street":"Basil Street",
                  "Suburb":"NEWPORT",
                  "State":"VIC",
                  "Postcode":"3015",
                  "Country":"Australia"
               }
            },
            {
               "Property":{
                  "ID":"39",
                  "Address":"Lorem ipsum dolor sit amet, consectetur",
                  "Address1":"Lorem ipsum dolor sit amet, consectetur",
                  "Address2":"Lorem ipsum dolor sit amet, consectetur",
                  "Bedrooms":"0",
                  "Bathrooms":"0",
                  "CarSpaces":"0",
                  "UnitNo":"3",
                  "StreetNo":"9",
                  "Street":"Basil Street",
                  "Suburb":"NEWPORT",
                  "State":"VIC",
                  "Postcode":"3015",
                  "Country":"Australia"
               }
            },
            {
               "Property":{
                  "ID":"37",
                  "Address":"Lorem ipsum dolor sit amet, consectetur",
                  "Address1":"Lorem ipsum dolor sit amet, consectetur",
                  "Address2":"Lorem ipsum dolor sit amet, consectetur",
                  "Bedrooms":"0",
                  "Bathrooms":"0",
                  "CarSpaces":"0",
                  "UnitNo":"3",
                  "StreetNo":"9",
                  "Street":"Basil Street",
                  "Suburb":"NEWPORT",
                  "State":"VIC",
                  "Postcode":"3015",
                  "Country":"Australia"
               }
            },
            {
               "Property":{
                  "ID":"38",
                  "Address":"Lorem ipsum dolor sit amet, consectetur",
                  "Address1":"Lorem ipsum dolor sit amet, consectetur",
                  "Address2":"Lorem ipsum dolor sit amet, consectetur",
                  "Bedrooms":"0",
                  "Bathrooms":"0",
                  "CarSpaces":"0",
                  "UnitNo":"2",
                  "StreetNo":"9",
                  "Street":"Basil Street",
                  "Suburb":"NEWPORT",
                  "State":"VIC",
                  "Postcode":"3015",
                  "Country":"Australia"
               }
            }
         ],
         "CommonProperty":{
            "Business":{
               "ID":"14",
               "AccountID":"1135",
               "PropertyID":"36",
               "ManagerID":"9",
               "Address":"Lorem ipsum dolor sit amet, consectetur",
               "StrataNumber":"Lorem ipsum dolor sit amet, consectetur",
               "NextAGM":"02/10/2013",
               "StartFinancialYear":"01/09/2013",
               "EndFinancialYear":"31/08/2014",
               "NextMeetingDate":"02/10/2013",
               "NextMeetingTime":"5:00 PM",
               "NextMeetingType":"Lorem ipsum dolor sit amet, consectetur",
               "NextMeetingBuilding":"Lorem ipsum dolor sit amet, consectetur",
               "NextMeetingAddress":"Lorem ipsum dolor sit amet, consectetur",
               "NextMeetingSuburb":"Lorem ipsum dolor sit amet, consectetur"
            }
         },
         "Strata":[
            {
               "Business":{
                  "ID":"17",
                  "AccountID":"1135",
                  "PropertyID":"37",
                  "ManagerID":"9",
                  "Address":"Lorem ipsum dolor sit amet, consectetur",
                  "Member":"Lorem ipsum dolor sit amet, consectetur",
                  "Fee":"354.33",
                  "Period":"Q",
                  "PaidTo":"01/09/2013",
                  "Credit":"0",
                  "LiabilityUnits":"100",
                  "EntitlementUnits":"105",
                  "LotNo":"1",
                  "FeeOutstanding":"0",
                  "OtherChargesOutstanding":"0",
                  "TotalOutstanding":"0",
                  "Manager":"Lorem ipsum dolor sit amet, consectetur",
                  "ManagerMobile":"0413 012 213",
                  "ManagerBusiness":"03-9982-1301",
                  "Manageremail":"test@sample.com",
                  "Committee":"N"
               }
            },
            {
               "Business":{
                  "ID":"19",
                  "AccountID":"1135",
                  "PropertyID":"38",
                  "ManagerID":"9",
                  "Address":"Lorem ipsum dolor sit amet, consectetur",
                  "Member":"Lorem ipsum dolor sit amet, consectetur",
                  "Fee":"354.33",
                  "Period":"Q",
                  "PaidTo":"30/11/2013",
                  "Credit":"0",
                  "LiabilityUnits":"100",
                  "EntitlementUnits":"90",
                  "LotNo":"2",
                  "FeeOutstanding":"0",
                  "OtherChargesOutstanding":"0",
                  "TotalOutstanding":"0",
                  "Manager":"Lorem ipsum dolor sit amet, consectetur",
                  "ManagerMobile":"0413 012 213",
                  "ManagerBusiness":"03-9982-1301",
                  "Manageremail":"test@sample.com",
                  "Committee":"N"
               }
            },
            {
               "Business":{
                  "ID":"21",
                  "AccountID":"1135",
                  "PropertyID":"39",
                  "ManagerID":"9",
                  "Address":"Lorem ipsum dolor sit amet, consectetur",
                  "Member":"Lorem ipsum dolor sit amet, consectetur",
                  "Fee":"354.34",
                  "Period":"Q",
                  "PaidTo":"01/09/2013",
                  "Credit":"0",
                  "LiabilityUnits":"100",
                  "EntitlementUnits":"105",
                  "LotNo":"3",
                  "FeeOutstanding":"354.34",
                  "OtherChargesOutstanding":"35.43",
                  "TotalOutstanding":"389.77",
                  "Manager":"Lorem ipsum dolor sit amet, consectetur",
                  "ManagerMobile":"1234567890",
                  "ManagerBusiness":"1234567890",
                  "Manageremail":"test@sample.com",
                  "Committee":"N"
               }
            }
         ],
         "Contacts":[
            {
               "Contact":{
                  "Relation":"Branch",
                  "ContactID":"1",
                  "IsCompany":"Y",
                  "FirstName":"Lorem ipsum dolor sit amet, consectetur",
                  "LastName":"Lorem ipsum dolor sit amet, consectetur",
                  "FullName":"Lorem ipsum dolor sit amet, consectetur",
                  "Mobile":"1234567890",
                  "eMail":"test@sample.com",
                  "BusinessID":"17",
                  "AccountID":"1135"
               }
            },
            {
               "Contact":{
                  "Relation":"Branch",
                  "ContactID":"1",
                  "IsCompany":"Y",
                  "FirstName":"Lorem ipsum dolor sit amet, consectetur",
                  "LastName":"Lorem ipsum dolor sit amet, consectetur",
                  "FullName":"Lorem ipsum dolor sit amet, consectetur",
                  "Mobile":"1234567890",
                  "eMail":"test@sample.com",
                  "BusinessID":"19",
                  "AccountID":"1135"
               }
            },
            {
               "Contact":{
                  "Relation":"Branch",
                  "ContactID":"1",
                  "IsCompany":"Y",
                  "FirstName":"Lorem ipsum dolor sit amet, consectetur",
                  "LastName":"Lorem ipsum dolor sit amet, consectetur",
                  "FullName":"Lorem ipsum dolor sit amet, consectetur",
                  "Mobile":"0418 316-554",
                  "eMail":"test@sample.com",
                  "BusinessID":"21",
                  "AccountID":"1135"
               }
            },
            {
               "Contact":{
                  "Relation":"Correspondence",
                  "ContactID":"40",
                  "IsCompany":"N",
                  "FirstName":"Lorem ipsum dolor sit amet, consectetur",
                  "LastName":"Lorem ipsum dolor sit amet, consectetur",
                  "FullName":"Lorem ipsum dolor sit amet, consectetur",
                  "Mobile":"1234567890",
                  "eMail":"test@sample.com",
                  "BusinessID":"17",
                  "AccountID":"1135"
               }
            },
            {
               "Contact":{
                  "Relation":"Correspondence",
                  "ContactID":"41",
                  "IsCompany":"N",
                  "FirstName":"Lorem ipsum dolor sit amet, consectetur",
                  "LastName":"Lorem ipsum dolor sit amet, consectetur",
                  "FullName":"Lorem ipsum dolor sit amet, consectetur",
                  "eMail":"test@sample.com",
                  "BusinessID":"19",
                  "AccountID":"1135"
               }
            },
            {
               "Contact":{
                  "Relation":"Correspondence",
                  "ContactID":"43",
                  "IsCompany":"N",
                  "FirstName":"Lorem ipsum dolor sit amet, consectetur",
                  "LastName":"Lorem ipsum dolor sit amet, consectetur",
                  "FullName":"Lorem ipsum dolor sit amet, consectetur",
                  "Mobile":"1234567890",
                  "eMail":"test@sample.com",
                  "BusinessID":"21",
                  "AccountID":"1135"
               }
            },
            {
               "Contact":{
                  "Relation":"Manager",
                  "ContactID":"9",
                  "IsCompany":"N",
                  "FirstName":"Lorem ipsum dolor sit amet, consectetur",
                  "LastName":"Lorem ipsum dolor sit amet, consectetur",
                  "FullName":"Lorem ipsum dolor sit amet, consectetur",
                  "Mobile":"1234567890",
                  "eMail":"test@sample.com",
                  "BusinessID":"17",
                  "AccountID":"1135"
               }
            },
            {
               "Contact":{
                  "Relation":"Manager",
                  "ContactID":"9",
                  "IsCompany":"N",
                  "FirstName":"Lorem ipsum dolor sit amet, consectetur",
                  "LastName":"Lorem ipsum dolor sit amet, consectetur",
                  "FullName":"Lorem ipsum dolor sit amet, consectetur",
                  "Mobile":"1234567890",
                  "eMail":"test@sample.com",
                  "BusinessID":"19",
                  "AccountID":"1135"
               }
            },
            {
               "Contact":{
                  "Relation":"Manager",
                  "ContactID":"9",
                  "IsCompany":"N",
                  "FirstName":"Lorem ipsum dolor sit amet, consectetur",
                  "LastName":"Lorem ipsum dolor sit amet, consectetur",
                  "FullName":"Lorem ipsum dolor sit amet, consectetur",
                  "Mobile":"1234567890",
                  "eMail":"test@sample.com",
                  "BusinessID":"21",
                  "AccountID":"1135"
               }
            },
            {
               "Contact":{
                  "Relation":"Member",
                  "ContactID":"40",
                  "IsCompany":"N",
                  "FirstName":"Lorem ipsum dolor sit amet, consectetur",
                  "LastName":"Lorem ipsum dolor sit amet, consectetur",
                  "FullName":"Lorem ipsum dolor sit amet, consectetur",
                  "Mobile":"1234567890",
                  "eMail":"test@sample.com",
                  "BusinessID":"17",
                  "AccountID":"1135"
               }
            },
            {
               "Contact":{
                  "Relation":"Member",
                  "ContactID":"41",
                  "IsCompany":"N",
                  "FirstName":"Lorem ipsum dolor sit amet, consectetur",
                  "LastName":"Lorem ipsum dolor sit amet, consectetur",
                  "FullName":"Lorem ipsum dolor sit amet, consectetur",
                  "eMail":"test@sample.com",
                  "BusinessID":"19",
                  "AccountID":"1135"
               }
            },
            {
               "Contact":{
                  "Relation":"Member",
                  "ContactID":"43",
                  "IsCompany":"N",
                  "FirstName":"Lorem ipsum dolor sit amet, consectetur",
                  "LastName":"Lorem ipsum dolor sit amet, consectetur",
                  "FullName":"Lorem ipsum dolor sit amet, consectetur",
                  "Mobile":"1234567890",
                  "eMail":"test@sample.com",
                  "BusinessID":"21",
                  "AccountID":"1135"
               }
            },
            {
               "Contact":{
                  "Relation":"OCSP:",
                  "ContactID":"38",
                  "IsCompany":"Y",
                  "LastName":"Lorem ipsum dolor sit amet, consectetur",
                  "FullName":"Lorem ipsum dolor sit amet, consectetur",
                  "eMail":"test@sample.com",
                  "BusinessID":"17",
                  "AccountID":"1135"
               }
            },
            {
               "Contact":{
                  "Relation":"OCSP:",
                  "ContactID":"38",
                  "IsCompany":"Y",
                  "LastName":"Lorem ipsum dolor sit amet, consectetur",
                  "FullName":"Lorem ipsum dolor sit amet, consectetur",
                  "eMail":"test@sample.com",
                  "BusinessID":"19",
                  "AccountID":"1135"
               }
            },
            {
               "Contact":{
                  "Relation":"OCSP:",
                  "ContactID":"38",
                  "IsCompany":"Y",
                  "LastName":"Lorem ipsum dolor sit amet, consectetur",
                  "FullName":"Lorem ipsum dolor sit amet, consectetur",
                  "eMail":"test@sample.com",
                  "BusinessID":"21",
                  "AccountID":"1135"
               }
            },
            {
               "Contact":{
                  "Relation":"PaymentFrom",
                  "ContactID":"40",
                  "IsCompany":"N",
                  "FirstName":"Anne",
                  "LastName":"Han Le",
                  "FullName":"Anne Han Le",
                  "Mobile":"0413 151-201",
                  "eMail":"test@sample.com",
                  "BusinessID":"17",
                  "AccountID":"1135"
               }
            },
            {
               "Contact":{
                  "Relation":"PaymentFrom",
                  "ContactID":"41",
                  "IsCompany":"N",
                  "FirstName":"Lorem ipsum dolor sit amet, consectetur",
                  "LastName":"Lorem ipsum dolor sit amet, consectetur",
                  "FullName":"Lorem ipsum dolor sit amet, consectetur",
                  "eMail":"test@sample.com",
                  "BusinessID":"19",
                  "AccountID":"1135"
               }
            },
            {
               "Contact":{
                  "Relation":"PaymentFrom",
                  "ContactID":"43",
                  "IsCompany":"N",
                  "FirstName":"Lorem ipsum dolor sit amet, consectetur",
                  "LastName":"Lorem ipsum dolor sit amet, consectetur",
                  "FullName":"Lorem ipsum dolor sit amet, consectetur",
                  "Mobile":"0411 733 198",
                  "eMail":"test@sample.com",
                  "BusinessID":"21",
                  "AccountID":"1135"
               }
            },
            {
               "Contact":{
                  "Relation":"Account Owner",
                  "ContactID":"38",
                  "IsCompany":"Y",
                  "LastName":"Lorem ipsum dolor sit amet, consectetur",
                  "FullName":"Lorem ipsum dolor sit amet, consectetur",
                  "eMail":"test@sample.com",
                  "BusinessID":"0",
                  "AccountID":"1135"
               }
            }
         ],
         "Insurance":{
            "Business":{
               "ID":"15",
               "AccountID":"1135",
               "PropertyID":"36",
               "Address":"Lorem ipsum dolor sit amet, consectetur",
               "Supplier":"Lorem ipsum dolor sit amet, consectetur",
               "RenewalDate":"06/09/2013",
               "PolicyName":"Lorem ipsum dolor sit amet, consectetur",
               "PolicyNumber":"123456890",
               "BuildingAmount":"897000",
               "PublicLiability":"10000000",
               "Premium":"1368.95",
               "Excess":"100",
               "VoluntaryWorkers":"250000"
            }
         }
      }
   }
}
```

### Sample Response

#### Success:

```
{
  "status": "success"
}
```

#### Error:

```
{
  "status": "error",
  "message": ""
}
```

####Note: 
> On Error message: use standard HTTP error codes but with some additional information.