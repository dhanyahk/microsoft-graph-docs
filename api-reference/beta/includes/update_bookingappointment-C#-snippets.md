
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var start = new DateTimeTimeZone
{
	@odata.type = "#microsoft.graph.dateTimeTimeZone",
	DateTime = "2018-05-06T15:00:00+03:00",
	TimeZone = "UTC",
};

var invoiceDate = new DateTimeTimeZone
{
	@odata.type = "#microsoft.graph.dateTimeTimeZone",
	DateTime = "2018-05-06T15:30:00+03:00",
	TimeZone = "UTC",
};

var end = new DateTimeTimeZone
{
	@odata.type = "#microsoft.graph.dateTimeTimeZone",
	DateTime = "2018-05-06T15:30:00+03:00",
	TimeZone = "UTC",
};

var appointments = new BookingAppointment
{
	@odata.type = "#microsoft.graph.bookingAppointment",
	End = end,
	InvoiceDate = invoiceDate,
	Start = start,
};

await graphClient.BookingBusinesses["Contosolunchdelivery@M365B489948.onmicrosoft.com"].Appointments["AAMkADKnAAA="]
	.Request()
	.UpdateAsync(appointments);

```