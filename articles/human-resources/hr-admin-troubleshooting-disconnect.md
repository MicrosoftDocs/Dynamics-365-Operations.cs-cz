---
title: Odpojení klienta
description: Tento článek vysvětluje, jak postupovat při bezdůvodném odpojení odběratele od jeho prostředí.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d02916283bbd4cee6502942020df1b275a0242b3
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111811"
---
# <a name="client-disconnects"></a>Odpojení klienta

**Podrobnosti o prostředí** 

Tento problém může nastat ve všech prostředích.
 
**Příznak** 

Odběratel je bezdůvodně odpojen od svého prostředí. Odběratel obdrží jednu z následujících chybových zpráv:

- Vaše připojení bylo ztraceno. Pokud chcete pokračovat v práci, klikněte na Zavřít.
- Zdá se, že se přerušilo připojení k síti. Akci opakujte kliknutím na tlačítko Opakovat.

**Závažný problém**

K tomuto problému dochází často, když uživatelé jsou ve fázi implementace, porovnávají informace v produkčních a testovacích prostředích a zapomínají, že se pohybují mezi relacemi. Pokud uživatelé jsou v této fázi, pravděpodobně se s tímto problémem setkají.

**Vydání** 

**Typy prohlížeče:** Google Chrome, Internet Explorer a Microsoft Edge

Microsoft Dynamics 365 Human Resources odpojuje uživatele, když jsou současně otevřeny dvě různé relace pro jednoho uživatele a stejný typ prohlížeče. (Například uživatel A zobrazuje prostředí 1 i 2 v prohlížeči Chrome.) Nezáleží na tom, zda uživatelé otevřenou jiná okna nebo jiné karty prohlížeče. Pokud se při přihlašování do prostředí 1 a prostředí 2 současně a ve stejném typu prohlížeče používají stejné přihlašovací údaje uživatele, aplikace Human Resources odpojí jednu z relací.

**Řešení**

Ujistěte se, že pro daný typ prohlížeče je současně otevřeno pouze jedno prostředí. Uživatelé mohou otevřít více relací do stejného prostředí (více záložek ve stejném prohlížeči).

Uživatelé, kteří chtějí přeskakovat mezi dvěma prostředími současně, by měli otevřít každé prostředí v jiném typu prohlížeče. (Například uživatel A může zobrazit prostředí 1 v Chrome a prostředí 2 v Microsoft Edge.)
