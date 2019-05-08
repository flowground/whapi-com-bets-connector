# ![LOGO](logo.png) Bets **flow**ground Connector

## Description

A generated **flow**ground connector for the Bets API (version 2.0.0).

Generated from: https://api.apis.guru/v2/specs/whapi.com/bets/2.0.0/swagger.json<br/>
Generated at: 2019-05-07T17:44:53+03:00

## API Description

The Bets API methods are used to place single, multiple and complex bets and to retrieve a customer’s bet history. When retrieving a customer’s bet history you can organize the bets from the betting history in terms of date, bet type and whether the bet is settled or not. You can also specify what fields to be included/excluded or return a list of all default fields the method returns. <br /><br /> The Bets API will also generate a bet delay if you’re placing a single/multiple bet in-Play by creating a time margin to negate the effects of major changes to the market (for example, goals during a football match). Note that in version 2 of our APIs, Bets API contains the functionality of both Bets API v1 and the Betslips API v1.

## Authorization

Supported authorization schemes:
- API Key
## Actions

### Places a multiple or a complex bet.

*Tags:* `Bets`

#### Input Parameters
* `apiSecret` - _required_ - Another unique identifier for your application.
* `apiTicket` - _required_ - The ticket obtained from the sessions API
* `fields` - _optional_ - Specify an absolute field list to return (Comma Separated List)
* `include` - _optional_ - Specify fields in addition to the default to return (Comma Separated List)
* `exclude` - _optional_ - Specify fields from the default to exclude (Comma Separated List)

### Places a single bet

> Places a single bet. When placing a single bet using live inplay bets, the system might generate a bet delay to allow a time margin to negate the effects of major changes (for example, goals) to the market.  Note that the amount of bet delay will vary by category and event type. A delayedBetId will be recieved that can be used to resubmit the bet.

*Tags:* `Bets`

#### Input Parameters
* `apiSecret` - _required_ - Another unique identifier for your application.
* `apiTicket` - _required_ - The ticket obtained from the sessions API
* `fields` - _optional_ - Specify an absolute field list to return (Comma Separated List)
* `include` - _optional_ - Specify fields in addition to the default to return (Comma Separated List)
* `exclude` - _optional_ - Specify fields from the default to exclude (Comma Separated List)

### Organises the betslip when one or more selections are made. It returns a bet slip structure organised by betting opportunities.

*Tags:* `Bets`

#### Input Parameters
* `apiSecret` - _required_ - Another unique identifier for your application.
* `apiTicket` - _required_ - The ticket obtained from the sessions API

### Returns available free bets

> Retrieves the current free bets available for a customer.

*Tags:* `Bets`

#### Input Parameters
* `apiSecret` - _required_ - Another unique identifier for your application.
* `apiTicket` - _required_ - The ticket obtained from the sessions API
* `fields` - _optional_ - Specify an absolute field list to return (Comma Separated List)
* `include` - _optional_ - Specify fields in addition to the default to return (Comma Separated List)
* `exclude` - _optional_ - Specify fields from the default to exclude (Comma Separated List)

### Retrieves the customer's bet history.

> Retrieves the customer's bet history. Options are available to organise the history in terms of date, bet type and settled and unsettled bets. The maximum number of bets and bet history pages retrieved can also be set.

*Tags:* `Bets`

#### Input Parameters
* `apiSecret` - _required_ - Another unique identifier for your application.
* `apiTicket` - _required_ - The ticket obtained from the sessions API
* `dateFrom` - _required_ - The UTC FROM datetime from bets to be returned. (yyyy-MM-ddTHH:mm:ss)
* `dateTo` - _required_ - The UTC TO datetime for bets to be returned. (yyyy-MM-ddTHH:mm:ss)
* `fields` - _optional_ - Specify an absolute field list to return (Comma Separated List)
* `include` - _optional_ - Specify fields in addition to the default to return (Comma Separated List)
* `exclude` - _optional_ - Specify fields from the default to exclude (Comma Separated List)
* `page` - _optional_ - The index of the page to return
* `pageSize` - _optional_ - The number of results per page
* `sort` - _optional_ - The order the response will be retuned by. i.e. transDateTime,desc. Only transDateTime can be used currently
* `settled` - _optional_ - Filter by settled bets. If omitted, both settled and unsettled will be returned.

### Allows a trusted application to cash in a bet (take a return on a bet) on behalf of the customer

> Allows a trusted application to cash in a bet (take a return on a bet) on behalf of the customer. If the customers monitor bets they can cash in a bet at any point before the event ends.

*Tags:* `Bets`

#### Input Parameters
* `apiSecret` - _required_ - Another unique identifier for your application.
* `apiTicket` - _required_ - The ticket obtained from the sessions API
* `betId` - _required_ - The identifier of the bet
* `cashInValue` - _required_ - The cash in value of the bet
* `cashinBetDelayId` - _required_ - The ID of this bet delay

## License

**flow**ground :- Telekom iPaaS / whapi-com-bets-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
