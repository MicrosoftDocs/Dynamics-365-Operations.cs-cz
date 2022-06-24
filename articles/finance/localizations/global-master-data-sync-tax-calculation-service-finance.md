---
title: Synchronizujte nastavení daně ze služby pro výpočet daně do aplikace Dynamics 365 Finance
description: Tento článek vysvětluje, jak synchronizovat kmenová data nastavení daně ze služby pro výpočet daně s Microsoft Dynamics 365 Finance.
author: wangchen
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegration, TaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: b017a19834998e1c493b0a38c1b50accd8c7e630
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853150"
---
# <a name="sync-the-tax-setup-from-the-tax-calculation-service-to-dynamics-365-finance"></a>Synchronizujte nastavení daně ze služby pro výpočet daně do aplikace Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje, jak synchronizovat kmenová data nastavení daně ze služby pro výpočet daně s Microsoft Dynamics 365 Finance.

Po provedení požadovaných kroků nastavení v [Začínáme s výpočtem daně](global-get-started-with-tax-calculation-service.md) budou následující data nastavení daně automaticky synchronizována ze služby pro výpočet daně do Finance.

## <a name="sales-tax-code"></a>Kód DPH

| Služba výpočtu daně           | Finance                             |
| --------------------------------- | ----------------------------------- |
| Kód daně                          | Kód DPH                      |
| Popis                       | Název                                |
| Uživatelský vstup                        | Období vyrovnání                   |
| Uživatelský vstup                        | Skupina zaúčtování hl. knihy                |
| Uživatelský vstup                        | Měna DPH                  |
| Je nakonfigurována záporná daňová sazba | Povolit záporné procento DPH |

## <a name="tax-value"></a>Hodnota daně

| Služba výpočtu daně | Finance                   |
| ----------------------- | ------------------------- |
| Od data transakce   | Od data                 |
| Do data transakce     | Do data                   |
| Minimální částka          | Minimální limit             |
| Maximální množství          | Maximální limit             |
| Sazba daně                | Hodnota                     |
| Neodpočitatelná sazba     | Neodpočitatelné procento |

## <a name="tax-limits"></a>Daňové limity

| Služba výpočtu daně | Finance           |
| ----------------------- | ----------------- |
| Od data transakce   | Od data         |
| Do data transakce     | Do data           |
| Minimální částka daně      | Min. DPH |
| Maximální částka daně      | Max. DPH |

## <a name="sales-tax-group"></a>Skupina DPH

| Služba výpočtu daně                         | Finance                                    |
| ----------------------------------------------- | ------------------------------------------ |
| Daňová skupina                                       | Skupina DPH                            |
| Daňové kódy v rámci této daňové skupiny                  | Kódy DPH v rámci této skupiny DPH |
| Daňový kód je označen jako **Je osvobozeno**         | Osvobození                                     |
| Daňový kód je označen jako **Je osvobozeno**         | Kód osvobození                                |
| Daňový kód je označen **Je přenesení daňové povinnosti** | Přenesená daňová povinnost                             |
| Daňový kód je označen jako **Je importní DPH**        | Importní DPH                                    |

## <a name="item-sales-tax-group"></a>Skupina DPH zboží

| Služba výpočtu daně             | Finance                                         |
| ----------------------------------- | ----------------------------------------------- |
| Skupina daně zboží                      | Skupina DPH zboží                            |
| Daňové kódy v rámci této daňové skupiny zboží | Kódy DPH v rámci této skupiny DPH zboží |

Po dokončení synchronizace pokračujte v udržování zbývajících parametrů v aplikaci Finance pro účely účtování a vykazování.

> [!NOTE]
> Synchronizace nastavení daně z Finance do služby pro výpočet daně není podporována. Pro existující prostředí Finance nejprve vytvořte nastavení daně ve službě pro výpočet daně. Poté synchronizujte data nastavení zpět do prostředí Finance.
