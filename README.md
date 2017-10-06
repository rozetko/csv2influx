# csv2influx

A tool for converting csv file to influxdb database.
You map csv fields to influxdb columns in config file.

#### In the development. Sorry, you can`t use it now. See the source code to use for your case

https://github.com/CorpGlory/csv2influx

## Install

```
npm install -g csv2influx
```

## Usage

```
csv2influx init        Creates template config file
csv2influx data.csv    Loads config file from current directory
                       then imports file data.csv to your influx
```

## Config documentation

```javascript

{
  influxdbUrl: "http://127.0.0.1:8086/INFLUXDB", // INFLUXDB database has to exists
  measurmentName: "MEASURMENT_NAME",
  mapping: {
    timestamp: "date",
    fieldShema: {
      date: {
        "format": "jsDate" // something what js can parse as string
      },
      lat: 'float',
      lng: 'float',
      name: 'string',
      description: 'string',
      location: 'string'
    },
  },
  csv: {
    delimiter: ','
  }
}

```

