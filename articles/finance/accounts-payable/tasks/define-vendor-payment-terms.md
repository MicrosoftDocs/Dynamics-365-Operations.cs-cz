---
title: Definování platebních podmínek dodavatelů
description: Toto téma vysvětluje, jak nastavit platební podmínky pro faktury dodavatele.
author: abruer
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7e6778f61a9367399e4b71d5b2bb2459c09ba508
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143884"
---
# <a name="define-vendor-payment-terms"></a>Definování platebních podmínek dodavatelů

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje, jak nastavit platební podmínky pro faktury dodavatele. Tento úkol využívá ukázkovou společnost USMF.

1. Přejděte do **Podokno navigace > Moduly > Závazky > Nastavení platby > Podmínky platby**.
2. Zvolte **Nové**. Stránku Podmínky platby lze použít pro definování způsobu výpočtu data splatnosti. Nepoužívá se při definování způsobu výpočtu data platební slevy.  
3. V poli **Platební podmínky** zadejte hodnotu.
4. Zadejte hodnotu do pole **Popis**.
5. Zadejte číslo do pole **Dny**. Číslo zadané v tomto poli se použije pro přidání k datu splatnosti nebo na konec období identifikované podle způsobu platby. Například když si zvolíte **Netto**, číslo bude přidáno do data splatnosti. Pokud vyberete možnost **Aktuální měsíc**, číslo se přidá k poslednímu dni aktuálního měsíce pro výpočet data splatnosti.  
6. Zvolte **Uložit**.
7. Zavřete stránku.
8. Přejděte do nabídky **Závazky > Nastavení platby > Platební slevy**.
9. Zvolte **Nové**.
10. V poli **Platební slevy** zadejte ID.
11. Zadejte hodnotu do pole **Popis**.
12. Pokud dodavatel nabízí vrstvenou slevu, vyberte následující platební slevu po vypršení platnosti aktuální.
13. Zavřete stránku.
14. Zadejte číslo do pole **Dny**. Množství zadané v poli **Dny** se použije k výpočtu data platební slevy, a to na základě možností vybraných v poli **Netto/Aktuální**. Pokud byla vybrána možnost **Netto**, množství bude přidáno k datu faktury pro určení data platební slevy. Pokud byla vybrána možnost **Aktuální měsíc**, množství bude přidáno ke konci aktuálního měsíce pro určení data platební slevy.  
15. Zadejte procentuální hodnotu platební slevy do pole **Sleva**. 
16. Zadejte hlavní účet, na který budou platební slevy zaúčtovány pro faktury odběratelů, a poté zadejte hlavní účet, na který budou platební slevy zaúčtovány pro faktury dodavatelů. Je-li hodnota **Slevové protiúčty** nastavena na **Použít hlavní účet pro slevu dodavatele**, použije se Hlavní účet. Pokud je možnost nastavena na **Účty na řádcích faktury**, platební sleva se zaúčtuje do účtů majetku / nákladů na řádky faktury.  
17. Zvolte **Uložit**.

