# Weather Data API
The Weather Data API is a web-based application programming interface (API) that allows users to access **European** historical weather data for a specific date.


## Data
The text file resources for this API are sourced from the [EUROPEAN CLIMATE ASSESSMENT & DATASET](https://www.ecad.eu/).

Currently, the API is using a smaller version of the text file data that is stored in the `data_small` folder. This folder contains 100 text files and each file contains daily weather data. In the future, we are looking to add a full data folder that will contain over 6,000 text files with weather data from all across Europe. The full data folder will contain more detailed weather data than the `data_small` folder, and it will cover a wider range of  measurements.

Please remember that the weather is limited to only some places from Europe and it is not a **global** dataset.


## API Endpoint

The API endpoint for accessing weather data is structured as follows:

- `http://127.0.0.1:5001`: This is the base URL of the API server. The `http://` prefix indicates that the server uses the HTTP protocol, and `127.0.0.1` is the IP address of the local host (i.e., the machine on which the server is running). The `:5001` specifies the port number on which the server is listening for requests.

- `/api/v1`: This is the path to the API endpoint. It consists of a series of segments separated by `/` characters. The `/api` segment indicates that this is an API endpoint, and the `/v1` segment indicates that this is the first version of the API.

- `<station>`: This is a placeholder for the station for which you want to retrieve weather data. You can specify the station using a numerical value (e.g., `10` for Station 10).

- `<year-month-day>`: This is a placeholder for the specific date for which you want to retrieve weather data. You can specify the date using the format `YYYY-MM-DD`, where `YYYY` is the four-digit year, `MM` is the two-digit month, and `DD` is the two-digit day.

## Example

To access the weather data for October 25, 1998 from Station 10, you can use the following URL:
http://127.0.0.1:5001/api/v1/10/1998-10-25 **(Currently this is on localhost so if you used it link you would not view anything)**

This will retrieve the weather data for October 25, 1998.

## Missing Values

In some cases, a particular weather measurement may not be available for a specific date. In these cases, the value for that measurement is indicated as `-9999`. This value should be interpreted as a missing value and should not be displayed.

## Thank you
