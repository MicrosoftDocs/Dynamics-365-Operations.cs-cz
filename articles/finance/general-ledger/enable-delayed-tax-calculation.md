---
title: Povolit výpočet opožděné daně v deníku
description: Toto téma vysvětluje, jak pomocí funkce **Povolit výpočet opožděné daně v deníku** zvýšit výkonnost výpočtu daně, pokud je objem řádků deníku velmi velký.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 5a8ae30a007d3e2b8b7a9bc9eb7786f6e58246d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176749"
---
# <a name="enable-delayed-tax-calculation-on-journal"></a>Povolit výpočet opožděné daně v deníku
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Toto téma vysvětluje, jak pomocí funkce **Povolit výpočet opožděné daně v deníku** zvýšit výkonnost výpočtu daně, pokud je objem řádků deníku velmi velký.

Aktuální chování při výpočtu DPH v deníku je v reálném čase spuštěno při aktualizaci polí daně, např. skupiny DPH nebo skupiny DPH položky. Každá aktualizace na úrovni řádku deníku znovu vypočítá částku daně na všech řádcích deníku. Pomáhá uživateli zobrazit vypočítanou částku daně v reálném čase, ale může také vést k potížím s výkonem v případě, že objem řádků deníku je velmi velký.

Tato funkce poskytuje možnost odložit výpočet daně za účelem vyřešení problému s výkonem. Je-li tato funkce zapnuta, bude částka daně vypočtena pouze v případě, že uživatel klikne na příkaz „DPH“ nebo zaúčtuje deník.

Uživatel může parametr zapnout nebo vypnout ve třech úrovních:
- Podle právnické osoby
- Dle názvu deníku
- Dle záhlaví deníku

Systém převezme hodnotu parametru v záhlaví deníku jako konečný. Hodnota parametru v záhlaví deníku bude převzata z názvu deníku. Hodnota parametru v názvu deníku bude při vytvoření názvu deníku přepsána z parametru hlavní knihy.

Je-li tento parametr zapnutý, skryje se pole ‚Skutečná částka DPH‘ a ‚Vypočítaná částka DPH‘ v deníku. Účelem je , aby nedošlo ke zmatení uživatele, protože hodnota těchto dvou polí vždy zobrazí 0 před spuštěním výpočtu daně uživatelem.

## <a name="enable-delayed-tax-calculation-by-legal-entity"></a>Povolit výpočet zpožděné daně podle právnické osoby

1. Přejděte do **Hlavní knihy > Nastavení hlavní knihy > Parametry hlavní knihy**
2. Klikněte na kartu **DPH**
3. Na pevné kartě **Obecné** vyhledejte parametr **Výpočet opožděné daně** a zapněte jej nebo vypněte.

![](media/delayed-tax-calculation-gl.png)



## <a name="enable-delayed-tax-calculation-by-journal-name"></a>Povolit výpočet opožděné daně dle názvu deníku

1. Přejděte do **Hlavní knihy > Nastavení deníku > Názvy deníků**
2. Na pevné kartě **Obecné** vyhledejte parametr **Výpočet opožděné daně** a zapněte jej nebo vypněte.

![](media/delayed-tax-calculation-journal-name.png)

## <a name="enable-delayed-tax-calculation-by-journal"></a>Povolit výpočet opožděné daně dle deníku

1. Přejděte do nabídky **Hlavní kniha > Položky deníku > Hlavní deníky**
2. Klepněte na možnost **Nový**
3. Vyberte název deníku.
4. Klikněte na možnost **Nastavení**
5. Vyhledej parametr **Výpočet opožděné daně** a zapněte jej nebo vypněte.

![](media/delayed-tax-calculation-journal-header.png)
