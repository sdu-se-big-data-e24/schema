# Consumption per Industry, Public and Private, Municipality and Hour
File: `consumption_per_industry_public_and_private_municipality_and_hour.avsc`
Source:  https://energidataservice.dk/tso-electricity/ConsumptionIndustry

| **Name**            | **Code name**  | **Type** | **Unit** | **Example**         | **Decode key** |
|---------------------|----------------|----------|----------|---------------------|----------------|
| Hour UTC            | HourUTC        | datetime |          | 2017-07-14T08:00    |                |      |      |      |      |
| Hour DK             | HourDK         | datetime |          | 2017-07-14T08:00:00 |                |      |      |      |      |
| Municipality number | MunicipalityNo | string   | Coded    | 101                 |                |      |      |      |      |
| Industry groups     | Branche        | string   |          | Erhverv             |                |      |      |      |      |
| Consumption kWh     | ConsumptionkWh | integer  | kWh      | 1234                | 18,1           |      |      |      |      |


# Production and Consumption - Settlement
File `production_and_consumption_settlement.avsc`
Source: https://energidataservice.dk/tso-electricity/ProductionConsumptionSettlement
| **Name**                          | **Code name**            | **Type** | **Unit**     | **Example**         | **Decode key**                      |
|-----------------------------------|--------------------------|----------|--------------|---------------------|-------------------------------------|
| Hour UTC                          | HourUTC                  | string   | datetime     | 2017-07-14T08:00:00 |                                     |
| Hour DK                           | HourDK                   | string   | datetime     | 2017-07-14T08:00:00 |                                     |
| Price area                        | PriceArea                | Enum     |              |                     | DK, DK1, DK2, DE, SE3, SE4, NO2, NL |
| Central Power                     | CentralPowerMWh          | integer  | MWh          | 5434                | 9,1 |
| Local Power                       | LocalPowerMWh            | integer  | MWh          | 651                 | 9,1 |
| CommercialPowerMWh                | CommercialPowerMWh       | integer  | MWh          | 1254                | 9,1 |
| Commercial power self-consumption | LocalPowerSelfConMWh     | integer  | MWh per hour | 6541                | 9,1 |
| Offshore Wind (<100MW) MWh        | OffshoreWindLt100MW_MWh  | integer  | MWh          | 1254                | 9,1 |
| Offshore Wind (>=100MW) MWh       | OffshoreWindGe100MW_MWh  | integer  | MWh          | 1254                | 9,1 |
| Onshore wind < 50 kW              | OnshoreWindLt50kW_MWh    | integer  | MWh          | 1254                | 9,1 |
| Onshore wind >= 50 kW             | OnshoreWindGe50kW_MWh    | integer  | MWh          | 1254                | 9,1 |
| Hydro Power MWh                   | HydroPowerMWh            | integer  | MWh          | 1254                | 9,1 |
| Solar power 0-10 kW               | SolarPowerLt10kW_MWh     | integer  | MWh          | 1254                | 9,1 |
| Solar power 10-40 kW              | SolarPowerGe10Lt40kW_MWh | integer  | MWh          | 1254                | 9,1 |
| Solar power over 40 kW            | SolarPowerGe40kW_MWh     | integer  | MWh          | 1254                | 9,1 |
| Solar power Self-consumption MWh  | SolarPowerSelfConMWh     | integer  | MWh          | 1254                | 9,1 |
| Unknown production MWh            | UnknownProdMWh           | integer  | MWh          | 1254                | 9,1 |
| Exchange of Energy to Norway      | ExchangeNO_MWh           | integer  | MWh          | 1254                | 9,1 |
| Exchange of Energy to Sweden      | ExchangeSE_MWh           | integer  | MWh          | 1254                | 9,1 |
| Exchange of Energy to Germany     | ExchangeGE_MWh           | integer  | MWh          | 1254                | 9,1 |
| Exchange of Energy to the Netherlands | ExchangeNL_MWh       | integer  | MWh          | 1254                | 9,1 |
| Exchange of Energy to Great Britain | ExchangeGB_MWh         | integer  | MWh          | 1254                | 9,1 |
| Exchange of Energy over the Great Belt | ExchangeGreatBelt_MWh | integer | MWh         | 1254                | 9,1 |
| Gross consumption                 | GrossConsumptionMWh      | integer  | MWh          | 1254                | 9,1 |
| Transmission Grid Loss            | GridLossTransmissionMWh  | integer  | MWh          | 1254                | 9,1 |
| Transmission Grid Loss, interconnectors | GridLossInterconnectorsMWh | integer | MWh   | 1254                | 9,1 |
| Distribution Grid Loss MWh        | GridLossDistributionMWh  | integer  | MWh          | 1254                | 9,1 |
| Power To Heat                     | PowerToHeatMWh           | integer  | MWh          | 1254                | 9,1 |

# Datahub Price List
File: `datahub_price_list.avsc`
Source: https://energidataservice.dk/tso-electricity/DatahubPricelist

| **Name**              | **Code name**        | **Type** | **Unit** | **Example**                          | **Decode key**                                                  |
|-----------------------|----------------------|----------|----------|--------------------------------------|-----------------------------------------------------------------|
| ChargeOwner           | ChargeOwner          | string   |          | Energi Fyn Net A/S - 554             |                                                                 |
| GLN Number            | GLN_Number           | string   |          | 5790000705689                        |                                                                 |
| Charge Type           | ChargeType           | string   |          | D03                                  | D01=Subscription, D02=Fee, D03=Tariff.                          |
| Charge Type Code      | ChargeTypeCode       | string   |          | 42106                                |                                                                 |
| Note                  | Note                 | string   |          | Reduceret PSO-tarif 100 GWh          |                                                                 |
| Description           | Description          | string   |          | Reduceret elafgift for elvarmekunder |                                                                 |
| Valid From            | ValidFrom            | date     |          | 25-12-2018                           |                                                                 |
| Valid To              | ValidTo              | date     |          | 25-12-2018                           |                                                                 |
| VAT Class             | VATClass             | string   |          | D01                                  |                                                                 |
| Prine [N]             | Price[N]             | integer  | DKK      | 0878000                              | N is 1-24 and represents hour of day. Integer format is: (12,6) |
| Transparent Invoicing | TransparentInvoicing | integer  |          | 0                                    | 0 or 1                                                          |
| Tax Indicator         | TaxIndicator         | integer  |          | 0                                    | 0 or 1                                                          |
| Resolution Duration   | ResolutionDuration   | string   |          | PT1H                                 |                                                                 |




# Power System Right Now
File: `power_system_right_now.avsc`
Source: https://energidataservice.dk/tso-electricity/PowerSystemRightNow