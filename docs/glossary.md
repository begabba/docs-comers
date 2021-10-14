# Glossary

This chapter tries explains some of the concepts and terminology used in the guides.

`Event`
: An bookable event in Comers consists of a connected `Project`, `Arrangement` & `Package`
Without execeptions we *always* use the exact same name for both `Project`, `Arrangement` & `Package`. Otherwise we're doomed.

`Project`
: A Project connects the Arrangement and Package together. A Project's `Project Number` is used as `resultat enhet` in Visma.
Projects can be used to filter searches via _Arrival list_ or _Search bookings_.

`Arrangement`
: Arrangements contains the price & capacity for the Arrangement part of a booking.
It also handles the presentation of the Package in the booking flow (description & image).
Arrangements has the same starting and ending date.

`Package`
: Package determines the bookable accommodations for the event. When events overlap the `Price type` is used make product only bookable for certain event.

`COMERS OVERVIEW`
: COMERS OVERVIEW is a Spreadsheet originally used to aid in creating event events for Comers. 

`Products`
: Products is Comers means beds for Ängsbacka. Is also refered to as Hotel. Products have a capacity & price just like Arrangements.

`Capacity`
: Both Arrangements & Products have capacity. Capacity decides the number of individuals (without infants) it can hold. `Allotment` means limited space and `Freesale` means unlimited.

`Price Type`:
: `Price Types` are an identifier used in `Packages` to tell Comers which products belong to which event. It's important that the `Price Type` is unique for each overlapping event. `AwesomeBar`'s Validate feature makes sure this is the case. Use `AB[0-9]` for participant events, `V[01-22]` for volunteer events and `LT0` for long term (renters/guests) events.

`AwesomeBar`
: This a set of features that runs in `COMERS OVERVIEW`. These can be accessed via the Ängsbacka menu. 

| AwesomeBar features | |
| -----------         | ------------------------------------                                            |
| Price               | Shows the arrangement & accommodation prices including early bird and discounts |
| Products            | View and edit assigned products to selected event                               |
| Validate            | Test the selected event for issues                                              |
| Capacity            | Compare capacity between the selected event in COMERS OVERVIEW and Comers       |



