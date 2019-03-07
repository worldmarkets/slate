## GetDepositInfo

**Category:** System<br />**Permissions:** Operator, Deposit<br />**Call Type:** Synchronous

Retrieves deposit key information so that the user can send cryptocurrency funds, and optionally generates new keys. The **GetDepositInfo** call is only for depositing cryptocurrency into an account.

Users with Deposit permission can deposit only to their own accounts; users with Operator permission can deposit to any account.

### Request

```json
{
    "OMSId": 1,
    "AccountId": 1,
    "ProductId": 1,
    "AccountProviderId": 1,
    "GenerateNewKey": true,
    "DepositInfo": "{}"
}
```

| Key               | Value                                                        |
| ----------------- | ------------------------------------------------------------ |
| OMSId             | **integer.** The ID of the Order Management System on which the deposit will be made. |
| AccountId         | **integer.** The ID of the account into which the deposit will be made. |
| ProductId         | **integer.** The ID of the product (asset) being deposited. **GetDepositInfo** is only for cryptocurrency deposits. |
| AccountProviderId | **integer.** The ID of the Account Provider that handles this specific product (asset). |
| GenerateNewKey    | **Boolean.** If *true*, **GetDepositInfo** generates two new keys. If *false,* **GetDepositInfo** reports the last two keys used. |
| DepositInfo       | **object.** A JSON object describing a deposit form template. The template may vary from Account Provider to Account Provider. You can obtain a list of templates available to you (and their contents) by calling **GetDepositRequestInfoTemplate** (you must have Operator or Trading permission). |

### Response

```json
["DepositKey1", "DepositKey2"]
```

The Response is an array of two crypto deposit keys, each a long integer. If the key *GenerateNewKey* in the Request has a *true* value, the two crypto deposit keys will be new; if the key *GenerateNewKey* has a *false* value, these will be the last two keys that were generated. 
