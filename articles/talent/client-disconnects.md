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
ms.openlocfilehash: 02df31b56c0e960a16ec2aadd8b1e817e0b6ec65
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898450"
---
# <a name="talent-client-disconnects"></a>Odpojení klienta aplikace Talent

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

Microsoft Dynamics 365 Talent odpojuje uživatele, když jsou současně otevřeny dvě různé relace pro jednoho uživatele a stejný typ prohlížeče. (Například uživatel A zobrazuje prostředí 1 i 2 v prohlížeči Chrome.) Nezáleží na tom, zda uživatelé otevřenou jiná okna nebo jiné karty prohlížeče. Pokud se při přihlašování do prostředí 1 a prostředí 2 současně a ve stejném typu prohlížeče používají stejné přihlašovací údaje uživatele, Talent odpojí jednu z relací.

**Řešení**

Ujistěte se, že pro daný typ prohlížeče je současně otevřeno pouze jedno prostředí. Uživatelé mohou otevřít více relací do stejného prostředí (více záložek ve stejném prohlížeči.

Uživatelé, kteří chtějí přeskakovat mezi dvěma prostředími současně, by měli otevřít každé prostředí v jiném typu prohlížeče. (Například uživatel A může zobrazit prostředí 1 v Chrome a prostředí 2 v Microsoft Edge.)
