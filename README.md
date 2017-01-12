# cosfaker
generate massive amounts of fake data for Intersystems Caché

## Usage

### On Populate

You can use on Populate event
`
Method OnPopulate() As %Status [ ServerOnly = 1 ]
{
	Set ..Login = ##class(cosFaker.Internet).UserName("John","Doe")
	Set ..Url = ##class(cosFaker.Internet).DomainWord()
}
`
Or on a simple Set

`Set ..Name = ##class(cosFaker.Name).FullName()`