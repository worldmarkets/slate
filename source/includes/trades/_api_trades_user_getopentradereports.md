## GetOpenTradeReports

**Category:** User<br />**Permissions:** Operator, Trading, AccountReadOnly<br/>**Call Type:** Synchronous

Retrieves an array of open trade information for the account named in *AccountId*. 

Users with Trading or AccountReadOnly permission must be associated with the named account; users with Operator permission can retrieve open trade reports on any account.

### Request

```json
{ 
  "OMSId": 1,
  "AccountId": 1
}
```

| Key       | Value                                                        |
| --------- | ------------------------------------------------------------ |
| OMSId     | **integer.** The ID of the Order Management System on which the account operates. |
| AccountId | **integer.** The ID of the account whose open trade information will be returned. |

### Response

```json
[
    {
        "Side": "Buy",
        "OrderId": 0,
        "Price":  0.0,
        "Quantity":  0.0,
        "DisplayQuantity":  0.0,
        "Instrument": 0,
        "Account": 0,
        "OrderType": "Unknown",
        "ClientOrderId": 0,
        "OrderState": "Unknown",
        "ReceiveTime": 0,
        "ReceiveTimeTicks": 0,
        "OrigQuantity": 0.0,
        "QuantityExecuted": 0.0,
        "AvgPrice": 0.0,
        "CounterPartyId": 0,
        "ChangeReason": "Unknown",
        "OrigOrderId": 0,
        "OrigClOrdId": 0,
        "EnteredBy": 0,
        "IsQuote": false,
        "InsideAsk": 0.0,
        "InsideAskSize": 0.0,
        "InsideBid": 0.0,
        "InsideBidSize": 0.0,
        "LastTradePrice": 0.0,
        "RejectReason": "",
        "IsLockedIn": false,
        "CancelReason": "",
        "OMSId": 0
    },
]
```

The call **GetOpenTradeReports** returns an array containing all four types of orders for the named account. The call returns an empty array if there are no open trades for the account.

| Key                               | Value                                                        |
| --------------------------------- | ------------------------------------------------------------ |
| Side                              | **string.** The side of a trade. One of:<br />**0** Buy<br />**1**  Sell<br />**2** Short<br />**3** Unknown (an error condition)   |
| OrderId                           | **long integer.** The ID of the open order. The *OrderID* is unique in each Order Management System. |
| Price                             | **real.** The price at which the buy or sell has been ordered. |
| Quantity                          | **real.** The quantity of the product to be bought or sold.  |
| DisplayQuantity                   | **real.** The quantity available to buy or sell that is publicly displayed to the market. To display a *displayQuantity* value, an order must be a Limit order with a reserve. |
| Instrument                        | **integer.** ID of the instrument being traded. The call  **GetInstruments** can supply the instrument IDs that are available. |
| orderType                         | **string.** Describes the type of order this is. One of:<br />**0** Unknown (an error condition)<br />**1** Market order<br />**2** Limit<br />**3** StopMarket<br />**4** StopLimit<br />**5** TrailingStopMarket<br />**6** TrailingStopLimit<br />**7** BlockTrade |
| ClientOrderId                     | **integer.** An ID supplied by the client to identify the order (like a purchase order number). The *ClientOrderId* defaults to 0 if not supplied.                       |
| OrderState                        | **string.** The current state of the order. One of:<br />**0** Unknown<br />**1** Working<br />**2** Rejected<br />**3** Canceled<br />**4** Expired<br />**5** Fully Executed.                           |
| ReceiveTime                       | **long integer.** Time stamp of the order in POSIX format.   |
| ReceiveTimeTicks                  | **long integer.** Time stamp of the order in POSIX format.   |
| OrigQuantity                      | **real.** If the open order has been changed or partially filled, this value shows the original quantity of the order.  |
| QuantityExecuted                  | **real.** If the open order has been at least partially executed, this value shows the amount that has been executed.  |
| AvgPrice                          | **real.** The average executed price for the instrument in the order.   |
| CounterPartyId                    | **integer.** The ID of the other party in an off-market trade.  |
| ChangeReason                      | **string.** If the order has been changed, this string value holds the reason. One of:<br />**0** Unknown<br />**1** NewInputAccepted<br />**2** NewInputRejected<br />**3** OtherRejected<br />**4** Expired<br />**5** Trade<br />**6** SystemCanceled_NoMoreMarket<br />**7** SystemCanceled_BelowMinimum<br />**8** SystemCanceled_PriceCollar<br />**9** SystemCanceled_MarginFailed<br />**100** UserModified  |
| OrigOrderId                       | **integer.** If the order has been changed, this is the ID of the original order.  |
| OrigClOrdId                       | **integer.** If the order has been changed, this is the ID of the original client order ID.  |
| EnteredBy                         | **integer.** The user ID of the person who entered the order.  |
| IsQuote                           | **Boolean.** If this order is a quote, the value for *IsQuote* is *true,* else *false.*  |
| InsideAsk                         | **real.** If this order is a quote, this value is the Inside Ask price.  |
| InsideAskSize                     | **real.** If this order is a quote, this value is the quantity of the Inside Ask quote.  |
| InsideBid                         | **real.** If this order is a quote, this value is the Inside Bid price.   |
| InsideBidSize                     | **real.** If this order is a quote, this value is the quantity of the Inside Bid quote.  |
| LastTradePrice                    | **real.** The last price that this instrument traded at.  |
| RejectReason                      | **string.** If this open order has been rejected, this string holds the reason for the rejection.  |
| IsLockedIn                        | **Boolean.** For a block trade, if both parties to the block trade agree that one of the parties will report the trade for both sides, this value is *true.* Othersise, *false.*  |
| CancelReason                      | **string.** If this order has been canceled, this string holds the cancelation reason.  |
| OMSId                             | **integer.** The ID of the Order Management System on which the order took place.  |

