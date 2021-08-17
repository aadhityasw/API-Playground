# COWIN API

The `COWIN` Web portal houses the real time date on the vaccine availability in centers throughout India. They also use this data to schedule vaccinations and keep track of all individual's vaccination information. All the real time data on vaccine availablity and the vaccination centers are made available through API's provided and managed by `APIsetu`. They also provide API's for the scheduling for vaccination through any of their centers, but we are currently not untilizing these features.

Here we will use the API's to list the states, districes, and also to get the real time list of all vaccination centers in a particular district.

This is a sample output JSON which is returned due to the API call made to the endpoint which is used to obtain the vaccination centers in a district. The following is a sample output with one center when the query is successful :

```json
{
  "sessions": [
    {
      "center_id": 1234,
      "name": "District General Hostpital",
      "name_l": "",
      "address": "45 M G Road",
      "address_l": "",
      "state_name": "Maharashtra",
      "state_name_l": "",
      "district_name": "Satara",
      "district_name_l": "",
      "block_name": "Jaoli",
      "block_name_l": "",
      "pincode": "413608",
      "lat": 28.7,
      "long": 77.1,
      "from": "09:00:00",
      "to": "18:00:00",
      "fee_type": "Paid",
      "fee": "250",
      "session_id": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
      "date": "31-05-2021",
      "available_capacity": 50,
      "available_capacity_dose1": 25,
      "available_capacity_dose2": 25,
      "walkin_ind": "Y",
      "min_age_limit": 18,
      "vaccine": "COVISHIELD",
      "slots": [
        "FORENOON",
        "AFTERNOON"
      ]
    }
  ]
}
```

**References**
* COWIN Portal : [cowin.gov.in](https://www.cowin.gov.in)
* APIsetu : [apisetu.gov.in](https://apisetu.gov.in/public/api/cowin/cowin-public-v2)
