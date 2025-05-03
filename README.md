# qb-vehiclesales
Used Car Sale for QB-Core Framework :blue_car:

# License

    QBCore Framework
    Copyright (C) 2021 Joshua Eger

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <https://www.gnu.org/licenses/>


## Dependencies
- [qb-core](https://github.com/qbcore-framework/qb-core)
- [qb-garages](https://github.com/qbcore-framework/qb-garages) - Vehicle ownership
- [qb-phone](https://github.com/qbcore-framework/qb-phone) - For the e-mail
- [qb-logs](https://github.com/qbcore-framework/qb-logs) - Keep event logs

## Screenshots
![Put Vehicle On Sale](https://imgur.com/bzE9e3o.png)
![Vehicle Sale Contract](https://imgur.com/A1ARcFV.png)
![Sell Vehicle To Dealer](https://imgur.com/zpEeBwk.png)
![Vehicle Sold Mail](https://imgur.com/vvz2UM3.png)
![Buy Vehicle](https://imgur.com/BEf5nDu.png)
![Vehicle Actions](https://imgur.com/HMuXtBd.png)

## Features
- Ability to put your vehicle on sale for other players to buy
- Ability to take your vehicle back if it is not sold yet
- Ability to sell your vehicle to the dealer for a fixed amount

## Installation
### Manual
- Download the script and put it in the `[qb]` directory.
- Import `qb-vehiclesales.sql` in your database
- Add the following code to your server.cfg/resouces.cfg
```
ensure qb-core
ensure qb-garages
ensure qb-phone
ensure qb-logs
ensure qb-vehiclesales
```

## Configuration
- To adjust tax, go to qb-vehiclesales\server\main.lua row 85 and change "77" to your liking
```
Config = Config or {}

Config.BlackListCars = { -- Add this table
    "t20",
}

Config.Zones = {
    ["SandyOccasions"] = {
        BusinessName = "Vehicle Sales Contract - Larry's Vehicle Sales",
        SellVehicle = vector4(1235.61, 2733.44, 37.4, 0.42),
        BuyVehicle = vector4(1213.31, 2735.4, 38.27, 182.5),

        PolyZone = {
            vector2(1338.3748779297, 2645.0153808594),
            vector2(1098.9381103516, 2621.7487792969),
            vector2(1117.9478759766, 2822.0729980469),
            vector2(1370.98828125, 2859.197265625)
        },
        MinZ = 36.0,
        MaxZ = 64.0,

        VehicleSpots = {
            vector4(1237.07, 2699, 38.27, 1.5),
            vector4(1232.98, 2698.92, 38.27, 2.5),
            vector4(1228.9, 2698.78, 38.27, 3.5),
            vector4(1224.9, 2698.51, 38.27, 2.5),
            vector4(1220.93, 2698.28, 38.27, 2.5),
            vector4(1216.97, 2698.05, 38.27, 0.5),
            vector4(1216.67, 2709.21, 38.27, 1.5),
            vector4(1220.67, 2709.26, 38.27, 1.5),
            vector4(1224.53, 2709.27, 38.27, 2.5),
            vector4(1228.52, 2709.42, 38.27, 1.5),
            vector4(1232.53, 2709.49, 38.27, 1.5),
            vector4(1236.71, 2709.51, 38.27, 1.6),
            vector4(1216.41, 2717.99, 38.27, 1.5),
            vector4(1220.39, 2718, 38.27, 0.5),
            vector4(1224.35, 2718.07, 38.27, 1.5),
            vector4(1228.41, 2718.22, 38.27, 1.5),
            vector4(1249.63, 2707.84, 38.27, 99.5),
            vector4(1248.92, 2712.25, 38.27, 101.5),
            vector4(1247.3, 2716.59, 38.27, 120.5),
            vector4(1244.09, 2720.4, 38.27, 149.5),
            vector4(1239.93, 2722.39, 38.27, 163.5),
            vector4(1248.28, 2727.41, 38.53, 338.5),
            vector4(1251.84, 2725.65, 38.52, 331.5),
            vector4(1255.19, 2723.21, 38.44, 309.5),
            vector4(1257.28, 2719.77, 38.49, 296.5),
        }
    }
}
```
