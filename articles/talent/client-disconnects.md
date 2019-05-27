---
title: Odpojení klienta aplikace Talent
description: Toto téma vysvětluje, jak postupovat při bezdůvodném odpojení odběratele od jeho prostředí.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 885e2d743cd2b01588546327840508f6f7e95958
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517483"
---
# <a name="talent-client-disconnects"></a>Odpojení klienta aplikace Talent

[!include [banner](includes/banner.md)]

**Podrobnosti o prostředí** 

Tento problém může nastat ve všech prostředích.
 
**Příznak** 

Odběratel je bezdůvodně odpojen od svého prostředí. Odběratel obdrží jednu z následujících chybových zpráv:

- Vaše připojení bylo ztraceno. Pokud chcete pokračovat v práci, klikněte na Zavřít.
- Zdá se, že se přerušilo připojení k síti. Akci opakujte kliknutím na tlačítko Opakovat.

**Závažný problém**

K tomuto problému dochází často, když uživatelé jsou ve fázi implementace, porovnávají informace v produkčních a testovacích prostředích a zapomínají, že se pohybují mezi relacemi. Pokud uživatelé jsou v této fázi, pravděpodobně se s tímto problémem setkají.

**Výdej** 

**Typy prohlížeče:** Google Chrome, Internet Explorer a Microsoft Edge

Platforma Microsoft Dynamics 365 for Talent odpojuje uživatele, když jsou současně otevřeny dvě různé relace pro jednoho uživatele a stejný typ prohlížeče. (Například uživatel A zobrazuje prostředí 1 i 2 v prohlížeči Chrome.) Nezáleží na tom, zda uživatelé otevřenou jiná okna nebo jiné karty prohlížeče. Pokud se při přihlašování do prostředí 1 a prostředí 2 současně a ve stejném typu prohlížeče používají stejné přihlašovací údaje uživatele, Talent odpojí jednu z relací.

**Řešení**

Ujistěte se, že pro daný typ prohlížeče je současně otevřeno pouze jedno prostředí. Uživatelé mohou otevřít více relací do stejného prostředí (více záložek ve stejném prohlížeči.

Uživatelé, kteří chtějí přeskakovat mezi dvěma prostředími současně, by měli otevřít každé prostředí v jiném typu prohlížeče. (Například uživatel A může zobrazit prostředí 1 v Chrome a prostředí 2 v Microsoft Edge.)
