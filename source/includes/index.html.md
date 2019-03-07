---

title: World Markets API Guide

language_tabs: # must be one of https://git.io/vQNgJ
  - json

toc_footers:
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes: # api - group - category - call
  - background/api_bkg_background
  - users/api_users_divider
  - users/api_users_act_activate2fa
  - users/api_users_user_adduseraffiliatetag
  - users/api_users_user_adduserinstrumentpermissions
  - users/api_users_user_adduserinstrumentpermissionsbulk
  - users/api_users_user_adduserproductpermissions
  - users/api_users_user_adduserproductpermissionsbulk
  - users/api_users_auth_authenticate2fa
  - users/api_users_auth_authenticateuser
  - users/api_users_user_canceluserreport
  - users/api_users_user_enablexp2fa
  - users/api_users_user_getl2snapshot
  - users/api_users_user_getlevel1
  - users/api_users_user_getuseraccountinfos
  - users/api_users_user_getuseraccounts
  - users/api_users_user_getuserreporttickets
  - users/api_users_user_getuserreportwriterresultrecords
  - users/api_users_auth_logout
  - users/api_users_user_removeuserproductpermissions
  - users/api_users_user_subscribeaccountevents
  - users/api_users_user_subscribelevel1
  - users/api_users_user_subscribelevel2
  - users/api_users_user_subscribeticker
  - users/api_users_user_subscribetrades
  - users/api_users_user_unsubscribelevel1
  - users/api_users_user_unsubscribelevel2
  - users/api_users_user_unsubscribeticker
  - users/api_users_user_unsubscribetrades
  - users/api_users_user_updateuseraffiliatetag
  - accounts/api_accts_divider
  - accounts/api_accts_user_generatetradeactivityreport
  - accounts/api_accts_user_generatetransactionactivityreport
  - accounts/api_accts_user_generatetreasuryactivityreport
  - accounts/api_accts_user_getaccountinfo
  - accounts/api_accts_user_getaccountledgerentry
  - accounts/api_accts_user_getaccountpositions
  - accounts/api_accts_user_gettreasuryproductsforaccount
  - accounts/api_accts_user_scheduletradeactivityreport
  - accounts/api_accts_user_scheduletransactionactivityreport
  - accounts/api_accts_user_scheduletreasuryactivityreport
  - trades/api_trades_divider
  - trades/api_trades_user_getaccounttrades
  - trades/api_trades_user_getaccounttransactions
  - trades/api_trades_user_getopentradereports
  - trades/api_trades_user_gettickerhistory
  - trades/api_trades_user_gettradeshistory
  - oms_orders/api_omsord_divider
  - oms_orders/api_omsord_user_cancelallorders
  - oms_orders/api_omsord_user_cancelorder
  - oms_orders/api_omsord_user_cancelquote
  - oms_orders/api_omsord_user_cancelreplaceorder
  - oms_orders/api_omsord_user_createquote
  - oms_orders/api_omsord_user_getopenorders
  - oms_orders/api_omsord_user_getopenquotes
  - oms_orders/api_omsord_user_getorderfee
  - oms_orders/api_omsord_user_getorderhistory
  - oms_orders/api_omsord_user_getorderhistorybyorderid
  - oms_orders/api_omsord_user_getordershistory
  - oms_orders/api_omsord_user_getorderstatus
  - oms_orders/api_omsord_user_modifyorder
  - oms_orders/api_omsord_user_sendorder
  - oms_orders/api_omsord_user_updatequote


  - products/api_products_divider
  - products/api_prods_user_getproduct
  - products/api_prods_user_getproductattributes
  - products/api_prods_user_getproducts

  - instrs/api_instrs_divider
  - instrs/api_instrs_user_getinstrument
  - instrs/api_instrs_user_getinstruments

  - tickets/api_tickets_divider

  - tickets/api_tix_system_acceptwithdrawticket
  - tickets/api_tix_system_adddepositticketattachment
  - tickets/api_tix_system_addwithdrawticketattachment
  - tickets/api_tix_system_cancelfailedwithdrawticket
  - tickets/api_tix_system_cancelwithdraw
  - tickets/api_tix_system_confirmwithdraw
  - tickets/api_tix_system_createassetmanagerwalletticket
  - tickets/api_tix_system_createdepositticket
  - tickets/api_tix_system_createwithdrawticket
  - tickets/api_tix_system_deposit
  - tickets/api_tix_user_getaccountdeposittransactions
  - tickets/api_tix_user_getaccountwithdrawtransactions
  - tickets/api_tix_system_getallassetmanagerwallettickets
  - tickets/api_tix_system_getalldeposittickets
  - tickets/api_tix_system_getalldepositrequestinfotemplates
  - tickets/api_tix_system_getallwithdrawtickets
  - tickets/api_tix_system_getassetmanagerwalletticket
  - tickets/api_tix_system_getdepositinfo
  - tickets/api_tix_system_getdepositrequestinfotemplate
  - tickets/api_tix_system_getdeposits
  - tickets/api_tix_system_getdepositticket
  - tickets/api_tix_system_getdepositticketattachment
  - tickets/api_tix_system_getdeposittickets
  - tickets/api_tix_system_getomswithdrawfees
  - tickets/api_tix_user_getwithdrawfee
  - tickets/api_tix_system_getwithdraws
  - tickets/api_tix_system_getwithdrawtemplate
  - tickets/api_tix_system_getwithdrawtemplatetypes
  - tickets/api_tix_system_getwithdrawticket
  - tickets/api_tix_system_getwithdrawticketattachment
  - tickets/api_tix_system_getwithdrawtickets
  - tickets/api_tix_system_markdepositticketasfullyprocessed
  - tickets/api_tix_system_markwithdrawticketascancelled
  - tickets/api_tix_system_markwithdrawticketasconfirmed
  - tickets/api_tix_system_markwithdrawticketasfullyprocessed
  - tickets/api_tix_system_resubmitfailedwithdrawticket
  - tickets/api_tix_system_submitdepositticketcomment
  - tickets/api_tix_system_submitwithdrawticketcomment
  - tickets/api_tix_system_updateassetmanagerwalletticket
  - tickets/api_tix_system_updatedepositticket
  - tickets/api_tix_system_updatewithdrawticket
  - tickets/api_tix_system_withdraw

  
  - uncertain/api_uncertain_divider
  - uncertain/api_uncert_user_getearliestticktime
  - uncertain/api_uncert_user_ping



 



 
search: true
---

# Introduction

This API covers the User-category calls in A5S digital asset platform software. It includes calls required for log-in and authentication.

### API URLs
Production - Streaming -  wss://wmapi.worldmarkets.io/WSGateway/

### Instrument ID's
BTC/USD   	1
ETH/USD		2
XRP/USD		3
LTC/USD		4
XMR/USD		5
IOTA/USD	6
BTAN/BTC	8
SWM/BTC		16
MTC/BTC		18
ORME/BTC	64
BCGC/BTC	118
SWEEP/BTC	119
PTX/BTC		120
PTX/ETH		121
TUBE/BTC	123
FLMI/BTC	124
PAT/BTC		125
SMT/BTC		126
FLASH/BTC	127
SPHTX/BTC	128
IXN/BTC		129
EBST/BTC	130
DDX/BTC		131
QUSD/BTC	132


### Revised calls
Generally, upper- and lowercase is not important for the key-value pairs inside a request or response. If an otherwise well formed call returns an unexpected error, check the case of the key-value pairs in the request.
