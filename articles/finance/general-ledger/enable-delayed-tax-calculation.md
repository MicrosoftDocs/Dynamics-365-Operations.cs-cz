---
title: Povolení výpočtu opožděné daně v denících
description: Tento článek vysvětluje, jak pomocí funkce Povolit výpočet výpočet opožděné daně v deníku zvýšit výkonnost výpočtu daně, pokud je objem řádků deníku velmi velký.
author: EricWang
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 02a038318d4c0fb44b6fcc4bb159ea87c2e9368a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887912"
---
# <a name="enable-delayed-tax-calculation-on-journals"></a>Povolení výpočtu opožděné daně v denících
[!include [banner](../includes/banner.md)]


V tomto článku je vysvětleno, jak lze zpozdit výpočet DPH v denících. Tato schopnost pomáhá zvýšit výkon při výpočtech daně v případě, že existuje mnoho řádků deníku.

Ve výchozím nastavení jsou částky DPH na řádcích deníku vypočteny při aktualizaci polí vztahujících se k dani. Mezi tato pole patří pole pro skupiny DPH a skupiny DPH položky. Jakákoli aktualizace řádku deníku způsobí přepočítání částek daně pro všechny řádky deníku. Ačkoli toto chování pomáhá uživateli zobrazit částky daně vypočtené v reálném čase, může také ovlivňovat výkonnost v případě, že je počet řádků deníku velmi velký.

Funkce výpočtu opožděné daně umožňuje zpozdit výpočet daně v denících, a proto může pomoci vyřešit problémy s výkonem. Je-li tato funkce zapnuta, budou částky daně vypočteny pouze v případě, že uživatel klikne na příkaz **DPH** nebo zaúčtuje deník.

Výpočet DPH můžete zpozdit ze tří úrovní:

- Právnická osoba
- Název deníku
- Záhlaví deníku

Systém dává prioritu nastavení pro záhlaví deníku. Ve výchozím nastavení je toto nastavení převzato z názvu deníku. Ve výchozím nastavení je nastavení názvu deníku převzato z nastavení na stránce **Parametry hlavní knihy** při vytvoření názvu deníku. V následujících oddílech je vysvětleno, jak zapnout výpočet zpožděné daně pro právnické osoby, názvy deníků a záhlaví deníků.

## <a name="turn-on-delayed-tax-calculation-at-the-legal-entity-level"></a>Zapnutí výpočtu opožděné daně na úrovni právnické osoby

1. Přejděte na **Hlavní kniha \> Nastavení hlavní knihy \> Parametry hlavní knihy**.
2. Na kartě **DPH** na pevné záložce **Obecné** nastavte možnost **Výpočet opožděné daně** na **Ano**.

![Obrázek Parametry hlavní knihy.](media/delayed-tax-calculation-gl.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-name-level"></a>Zapnutí výpočtu opožděné daně na úrovni názvu deníku

1. Přejděte na položky **Hlavní kniha \> Nastavení deníku \> Názvy deníku**.
2. Na pevné záložce **Obecné** v části **DPH** nastavte možnost **DVýpočet opožděné daně** na **Ano**.

![Obrázek Názvy deníků.](media/delayed-tax-calculation-journal-name.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-header-level"></a>Zapnutí výpočtu opožděné daně na úrovni záhlaví deníku

1. Přejděte na **Hlavní kniha \> Položky deníku \> Hlavní deníky**.
2. Zvolte **Nové**.
3. Vyberte název deníku.
4. Na kartě **Nastavení** nastavte možnost **Výpočet opožděné daně** na hodnotu **Ano**.

![Obrázek stránky hlavního deníku.](media/delayed-tax-calculation-journal-header.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
