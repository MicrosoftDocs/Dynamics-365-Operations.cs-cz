---
title: Výpočet TDS na fakturách
description: Toto téma poskytuje referenci k transakcím, kde se daň odečtená u zdroje (TDS) počítá na úrovni faktury.
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
ms.openlocfilehash: 496e87e3028025f738d2f0a697d91c18b77ad1c9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023092"
---
# <a name="tds-calculation-on-invoices"></a>Výpočet TDS na fakturách

[!include [banner](../includes/banner.md)]

Toto téma poskytuje referenci k transakcím, kde se daň odečtená u zdroje (TDS) počítá na úrovni faktury.

| Sériové číslo | Typ transakce                                 | Částka transakce | Název stránky a cesta výběru                                 | Typ účtu a typ protiúčtu                         |
| ------------- | ------------------------------------------------ | ------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1.            | Nákup uskutečněný od dodavatele / záznam nákladů   | Má dáti nebo Dal  | Stránka Obecné deníky (Hlavní kniha > Položky deníku > Obecné deníky), stránka deníku schválení faktury (Závazky > Faktury> Schválení faktury), stránka deníku faktury (Závazky >Faktury > Deník faktur) | Hlavní kniha (Dr.), Dodavatel (Cr.).  Srážková daň se počítá pro kombinaci dodavatel – hlavní kniha pouze v případě, že účet hlavní knihy má typ zaúčtování **Nákup** **hotovost**. |
| 2.            | Nákup uskutečněný od zákazníka / záznam nákladů | Má dáti nebo Dal  | Stránka Obecné deníky (Hlavní kniha > Položky deníku > Obecné deníky), stránka deníku faktury (Závazky > Faktury> Deník faktur) | Hlavní kniha (Dr.), zákazník (Cr.)                                 |
| 3.            | Nákup dlouhodobého majetku od dodavatele              | Má dáti nebo Dal  | Stránka Obecné deníky (Hlavní kniha > Položky deníku > Obecné deníky), stránka deníku registrace faktury (Závazky > Faktury> Registrace faktury), stránka deníku faktury (Závazky >Faktury > Deník faktur) | Dlouhodobý majetek (Dr.) Dodavatel (Cr.)                             |
| 4.            | Nákup dlouhodobého majetku od zákazníka            | Má dáti nebo Dal  | Stránka Obecné deníky (Hlavní kniha > Položky deníku > Obecné deníky), stránka deníku faktury (Závazky > Faktury> Deník faktur) | Dlouhodobý majetek (Dr.) Zákazník (Cr.)                           |
| 5.            | Nákupní faktura (závazek TDS)                  |                    | Stránka Nákupní objednávky (Závazky > Nákupní objednávky > Všechny nákupní objednávky) |                                                              |
| 6.            | Prodejní faktura (pohledávka TDS)                  |                    | Stránka prodejní objednávky (Pohledávky> Objednávky > Všechny prodejní objednávky), stránka faktury s volným textem (Pohledávky> Faktury > Všechny faktury s volným textem) |                                                              |
