---
title: Návrhář vzorců pro výpočty TDS
description: Toto téma poskytuje příklad způsobu výpočtu daně odečtené u zdroje (TDS) na základě vzorce definovaného pro každý daňový kód TDS ve skupině TDS, která je připojena k transakci.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: e9c97982233b1f3dc3924fa42954b5cb8d09ffcaa07d19a3892b25737a6c29c5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778862"
---
# <a name="formula-designer-for-tds-calculations"></a>Návrhář vzorců pro výpočty TDS

[!include [banner](../includes/banner.md)]

Toto téma poskytuje příklad způsobu výpočtu daně odečtené u zdroje (TDS) na základě vzorce definovaného pro každý daňový kód TDS. Daňové kódy TDS jsou definovány ve skupině TDS, která je připojena k transakci. Před navrhováním vzorců TDS proveďte základní nastavení požadované pro TDS, jak je uvedeno v následujících krocích. 

- Nastavte skupiny složek TDS na stránce **Skupiny složek srážkové daně**. 
- Nastavte komponenty TDS a připojte skupinu komponent TDS ke komponentám TDS pomocí stránky **Složky srážkové daně**. 
- Nastavte daňové kódy TDS a připojte skupinu komponent TDS k daňovým kódům pomocí stránky **Kódy srážkové daně**. 
- Nastavte daňové skupiny TDS na stránce **Skupiny složek srážkové daně**. Poté připojte daňové kódy TDS k daňové skupině a definujte vzorec pomocí stránky **Návrhář vzorců**. 

**Příklad vzorce**

V tomto příkladu je skupina TDS, Pronájem, připojena k nákupní faktuře, která je vytvořena pro dodavatele A. Částka faktury je 100 000 $. V následující tabulce najdete výpočet TDS pro fakturu.

| Skupina TDS                                                   | Daňové kódy TDS připojené ke skupině TDS | Hodnota              | Zdanitelný základ (návrhář vzorců) | Výpočetní výraz (Návrhář vzorců) | Základní částka | Vypočtená částka TDS |
| ------------------------------------------------------------ | --------------------------------------- | ------------------ | --------------------------------- | :----------------------------------------: | ----------- | --------------------- |
| Renta                                                         | TDS (Složka TDS – TDS)                | 10 %                | Hrubá částka                      |                                            | 100,000      | 10,000                 |
| Příplatek (složka TDS – příplatek)                         | 10 %                                     | Mimo hrubou částku | +TDS                              |                   10000                    | 1 000        |                       |
| PE-Cess (složka TDS – PE-Cess)                            | 2 %                                      | Mimo hrubou částku | + TDS + Příplatek                    |                   11000                    | 220         |                       |
| SHE Cess (složka TDS – SHE Cess)                          | 1 %                                      | Mimo hrubou částku | + TDS + Příplatek                    |                   11000                    | 110         |                       |
| **Celková** **TDS** **vypočtená** **pro** **fakturu** | **11,330**                               |                    |                                   |                                            |             |                       |

Položky dokladu jsou vytvořeny následovně.

| Účet           | Debet  | Kredit |
| ----------------- | ------ | ------ |
| Renta              | 100,000 |        |
| Dodavatel A          |        | 100,000 |
| Dodavatel A          | 11,330  |        |
| Splatná TDS       |        | 10,000  |
| Splatný příplatek |        | 1 000   |
| Splatné PE-Cess   |        | 220    |
| Splatné SHE-Cess  |        | 110    |
