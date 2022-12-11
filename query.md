# Team: Team 404/2

## create new booking

- `mutation { newBooking(vehicle_id:"5e66836ed654d5772d4eea59", booking_price:50, start_time: "2020-03-13 10:20:0", end_time: "2020-03-13 10:20:0"){ id, make } }`

## remove booking

- `mutation { delBooking(booking_id:"5e6bcccf3d376e6747c358d2"){ id } }`

## update booking

- `mutation { updateBooking(id:"5e6c7c2f0a745f05e6877b85", booking_price:20, start_time: "2020-03-9 10:20:0", end_time: "2020-03-10 10:20:0") { id } }`

## add location

- `mutation { addLocation(name:"SJSU", address:"San Jose", capacity: 100) { name } }`

## get location

- `query { location(id:"5e6d9ca8894d1a9cc1ea227b") { id, } }`

## update Location

- `mutation { updateLocation(id:"5e6db0889d8599220c1cc575" , name: "San Jose" , address:"Shanghai", capacity:200) { id } }`

## remove location

- `mutation { delLocation(location_id:"5e6daf939d8599220c1cc574"){ id } }`

## get contract

- `query { contract(id:"5e6ec07d623a71c7656614e1") { id, total_price } }`

## newUser

- `mutation{ newUser( email: "shengtaoli0110+t3@gmail.com", password: "welcome1", username: "shengtaoli0110+t0", address: "123 Foo Bar", dl_state: "CA", dl_number: "4343wer", mobile_phone: "1234567773", age: 30, registration_date: "2010-01-01 00:00:00", credit_card_info: { credit_card_number: "12312312312" card_holder_name: "Stan Li" billing_address: "123 Foo Bar" exp_date: "2022-01-01 00:00:00" }, membership: { start_date: "2010-01-01 00:00:00", last_renew_date: "2010-01-01 00:00:00" is_active: true }, role: "Admin", is_active: true ) { token } }`

## login

- `query{ login(email: "shengtaoli0110+t3@gmail.com",pw:"welcome1"){ token } }`

## http header example

- `{"Authorization": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZTgwMTBlNTgzYWVhMjg5NjZmM2M1NGIifQ.CJGvgFk7hFNJ_dao8a5-NCKKmlwqBWm7N2xqinCPzPQ"}`

id: 5eaa32f09bed907c0b2f67bd ,shengtaoli0110+t6@gmail.com
"eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZWFhMzJmMDliZWQ5MDdjMGIyZjY3YmQifQ.VJ9MhfB9fpvc6m6X_xyJXGEI3Hl7jPo1JZYRkBKgvL0"

id: "5eac55c80635cad3f4e975ff" shengtaoli0110+t7@gmail.com
"eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZWFjNTVjODA2MzVjYWQzZjRlOTc1ZmYifQ.gbBuJsuKrE_E0DfH6Q9cyGrBiZwYqB-8ImqxpiYYnk8"

# generate unpaid reservation

mutation {
generate_unpaid_reservation(
vehicle_id:"5eaa22f519233efdd874efd9", start_time: "2020-03-9 10:20:0", end_time: "2020-03-10 10:20:0")
{
start_time
}
}

# pay the reservation

mutation {
user_pay_reservation(id: "5eaa352e09601bcc48c69199"){
start_time
status
id
}
}

# add reservation according token

mutation {
token_add_reservation(
vehicle_id:"5eaa22f519233efdd874efd9", start_time: "2020-03-8 10:20:0", end_time: "2020-03-10 10:20:0")
{
start_time
}
}

# add Vehicle

mutation{
addVehicle(vehicle_type:"5e97e27475ac6f8a20c48c0d",
model:"focus", default_hourly_rate: 1.2, make:"Ford",year:2013,
registration_tag:"regiestered", current_mileage: 2000.1, condition:"good", capacity:5, images:"test" ) {
condition
}
}
