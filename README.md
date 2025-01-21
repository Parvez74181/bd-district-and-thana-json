# Bangladesh District and Thana Data

This repository contains JSON data representing the districts and their respective thanas (sub-districts) in Bangladesh. This data can be used in various applications such as web development projects, mobile apps, data analysis, and more.

## Motivation

I needed thana and district data for one of my projects, but I couldn't find any suitable resource. Therefore, I created the JSON file myself. With the advent of AI, I took help from ChatGPT to write the names of the thanas in Bengali.


## Data Structure

The JSON data is organized as follows:

```json
{
  "districts": [
    {
      "districtEn": "District Name",
      "districtBn": "ডিস্ট্রিকট বাংলা নাম",

      "thana": [
        {
          "english_name": "Thana English Name",
          "bangla_name": "থানা বাংলা নাম"
        },
        {
          "english_name": "Thana English Name",
          "bangla_name": "থানা বাংলা নাম"
        },
        ...
      ]
    },
    ...
  ]
}
```

- **district**: An array containing objects representing each district.
  - **district**: The name of the district.
  - **thana**: An array containing objects representing each thana within the district.
    - **english_name**: The English name of the thana.
    - **bangla_name**: The Bangla name of the thana.

## Usage

You can use this data in your projects by fetching the JSON file from this repository. Here's how you can access the data using JavaScript:

```javascript
// Example using Axios (assuming you're using a frontend framework or Node.js)
axios.get('bd-district-and-thana.json')
  .then(response => {
    const districtData = response.data;
    // Use the data as needed
  })
  .catch(error => {
    console.error('Error fetching district data:', error);
  });
```

```javascript
// Example using fetch
fetch('bd-district-and-thana.json')
  .then(response => {
    if (!response.ok) {
      throw new Error('Network response was not ok');
    }
    return response.json();
  })
  .then(data => {
    // Work with the data
    console.log(data);
  })
  .catch(error => {
    console.error('Error fetching district data:', error);
  });

```

## Contributing

Contributions to improve the data or add more details are welcome! If you find any errors or missing information, please open an issue or submit a pull request with your changes.

## License

This data is provided under the Creative Commons Attribution-ShareAlike 4.0 International License. You are free to share and adapt the data for any purpose, even commercially, as long as you give appropriate credit and distribute your contributions under the same license.

## Acknowledgements

The data in this repository is sourced from various governmental and public domain resources. We would like to acknowledge the efforts of those who collected and compiled this information.
