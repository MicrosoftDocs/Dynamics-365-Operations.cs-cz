---
title: Výpočet TDS na fakturách
description: Tento článek poskytuje referenci k transakcím, kde se daň odečtená u zdroje (TDS) počítá na úrovni faktury.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: efc12e0839fe87e9db435f481ce1fd733c286d6c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855356"
---
# <a name="tds-calculation-on-invoices"></a>Výpočet TDS na fakturách

[!include [banner](../includes/banner.md)]

Tento článek poskytuje referenci k transakcím, kde se daň odečtená u zdroje (TDS) počítá na úrovni faktury.

| Sériové číslo | Typ transakce                                 | Částka transakce | Název stránky a cesta výběru                                 | Typ účtu a typ protiúčtu                         |
| ------------- | ------------------------------------------------ | ------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1.            | Nákup uskutečněný od dodavatele / záznam nákladů   | Má dáti nebo Dal  | Stránka Obecné deníky (Hlavní kniha > Položky deníku > Obecné deníky), stránka deníku schválení faktury (Závazky > Faktury> Schválení faktury), stránka deníku faktury (Závazky >Faktury > Deník faktur) | Hlavní kniha (Dr.), Dodavatel (Cr.).  Srážková daň se počítá pro kombinaci dodavatel – hlavní kniha pouze v případě, že účet hlavní knihy má typ zaúčtování **Nákup** **hotovost**. |
| 2.            | Nákup uskutečněný od zákazníka / záznam nákladů | Má dáti nebo Dal  | Stránka Obecné deníky (Hlavní kniha > Položky deníku > Obecné deníky), stránka deníku faktury (Závazky > Faktury> Deník faktur) | Hlavní kniha (Dr.), zákazník (Cr.)                                 |
| 3.            | Nákup dlouhodobého majetku od dodavatele              | Má dáti nebo Dal  | Stránka Obecné deníky (Hlavní kniha > Položky deníku > Obecné deníky), stránka deníku registrace faktury (Závazky > Faktury> Registrace faktury), stránka deníku faktury (Závazky >Faktury > Deník faktur) | Dlouhodobý majetek (Dr.) Dodavatel (Cr.)                             |
| 4.            | Nákup dlouhodobého majetku od zákazníka            | Má dáti nebo Dal  | Stránka Obecné deníky (Hlavní kniha > Položky deníku > Obecné deníky), stránka deníku faktury (Závazky > Faktury> Deník faktur) | Dlouhodobý majetek (Dr.) Zákazník (Cr.)                           |
| 5.            | Nákupní faktura (závazek TDS)                  |                    | Stránka Nákupní objednávky (Závazky > Nákupní objednávky > Všechny nákupní objednávky) |                                                              |
| 6.            | Prodejní faktura (pohledávka TDS)                  |                    | Stránka prodejní objednávky (Pohledávky> Objednávky > Všechny prodejní objednávky), stránka faktury s volným textem (Pohledávky> Faktury > Všechny faktury s volným textem) |                                                              |
