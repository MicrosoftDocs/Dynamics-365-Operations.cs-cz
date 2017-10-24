---
title: "Výpočty pro modely konfigurace produktu - často kladené dotazy"
description: "Tento článek popisuje výpočty pro modely konfigurace produktu a vysvětluje, jak použít výpočty spolu s omezeními."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCConstraintEditor, PCProductConfigurationModelDetails, PCRuntimeConfigurator
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19191
ms.assetid: 8993f9a1-d1c0-49f5-afd3-5e1077ded0fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fea4e139d32c780769bafe08d603b828d366550c
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="calculations-for-product-configuration-models-faq"></a>Výpočty pro modely konfigurace produktu - často kladené dotazy

[!include[banner](../includes/banner.md)]


Tento článek popisuje výpočty pro modely konfigurace produktu a vysvětluje, jak použít výpočty spolu s omezeními.

Výpočty lze použít pro aritmetické nebo logické operace. Doplňují omezení výrazu v modelech konfigurace produktu. Je možné určit výpočty na stránce **Podrobnosti modelu produktu s konfigurací založenou na omezeních** a pak vytvořit výrazy pro výpočty v editoru výrazu. Další informace viz Vytvořit výpočty.

## <a name="what-is-a-calculation"></a>Co je výpočet?
Výpočet je prvek, který můžete použít v modelu konfigurace produktu. Výpočty doplňují omezení tak, že vám při konfiguraci produktu umožňují pomocí desetinných čísel vypočítat hodnoty. Kromě toho výpočty mají k dispozici větší sadu operátorů než omezení.  

Podobně jako omezení je výpočet přidružen k určité součásti ve modelu konfigurace produktu a nelze ho znovu použít nebo sdílet s jinou součástí. Jeden důležitý rozdíl mezi výpočty a omezení, je, že výpočty jsou imperativní (jednosměrné), zatímco omezení jsou deklarativní (obousměrné). Další informace o omezení viz [Omezení výrazu a omezení tabulky](expression-constraints-table-constraints-product-configuration-models.md).  

Výpočet se skládá z cílového atributu a vzorce výpočtu.

## <a name="what-is-a-target-attribute"></a>Co je cílový atribut?
Cílový atribut je atribut, který přijme výsledek výpočtu ve výrazu.  

V následujícím výrazu je cílový atribut měření ubrusu:  

**Výraz:** If\[decimalAttribute1 &lt;= decimalAttribute2, True, False\]  

**DecimalAttribute1** je délka stolu a **decimalAttribute2** je délka ubrusu. Výraz vrací hodnotu **True** do cílového atributu, pokud je **decimalAttribute2** větší nebo roven **decimalAttribute1**. V opačném případě se výraz vrací hodnotu **Nepravda**. Měření ubrusu je tedy přípustné, pokud je délka ubrusu rovná nebo překračuje délku stolu.

## <a name="what-attribute-types-can-be-set-to-target-attributes"></a>Které typy atributů lze nastavit jako cílové atributy?
Všechny typy atributů, které jsou podporovány pro konfigurátor výrobku lze nastavit jako cílové atributy kromě textu bez pevného seznamu.

## <a name="can-the-value-of-a-target-attribute-restrict-the-values-of-the-input-attributes-in-a-calculation"></a>Může hodnota pro cílový atribut omezit hodnoty vstupních atributů ve výpočtu?
Ne. Hodnota pro cílový atribut nemůže omezit hodnoty vstupních atributů, protože výpočty jsou jednosměrné. Proto je hodnota cílového atributu nastavena podle změny hodnoty u vstupních atributů, ale změna hodnoty cíle neovlivní hodnotu vstupních atributů. Toto chování se liší od chování omezení. K omezení dochází oběma směry.

### <a name="example"></a>Příklad

V následujícím výrazu je cíl pro výpočet délka napájecího kabelu a vstupní hodnota je barva:  

**Výraz:** \[If Color == "Green", 1.5, 1.0\]  

Při konfiguraci položky je délka napájecího kabelu nastavena na **1.5**, zadáte-li **Green** jako hodnotu atributu barvy. Pokud zadáte libovolnou jinou barvu, délka je nastavena na **1,0**. Vzhledem k tomu, že jsou výpočty jednosměrné, však výpočet nenastaví hodnotu atributu barva na **Zelená** při zadání délky **1,5**.

## <a name="what-happens-if-a-calculation-has-a-target-attribute-of-the-integer-type-but-a-calculation-generates-a-decimal-number"></a>Co se stane, má-li výpočet cílový atribut typu celé číslo, ale výpočet poskytne desetinné číslo?
Pokud cílový atribut je celé číslo, ale výpočet vygeneruje desetinné číslo, bude vrácena pouze část „celé číslo“ z výsledného výpočtu. Desetinná část bude odebrána, a výsledek nebude zaokrouhlen. Například výsledek 12,70 se zobrazí jako 12.

## <a name="when-do-calculations-occur"></a>Kdy dojde k výpočtům?
Výpočet proběhne při zadání hodnoty všech vstupních atributů.

## <a name="can-i-overwrite-the-value-that-is-calculated-for-the-target-attribute"></a>Lze přepsat hodnotu, která byla vypočtena pro cílový atribut?
Můžete přepsat hodnotu, která byla vypočtena pro cílový atribut, ledaže by byl cílový atribut nastaven jako skrytý nebo jen pro čtení.

## <a name="how-do-i-set-a-target-attribute-as-hidden-or-readonly"></a>Jak nastavím cílový atribut jako skrytý nebo jen pro čtení?
Pokud chcete nastavit atribut jako skrytý nebo jen pro čtení, postupujte takto.

1.  Klikněte na **Řízení informací o produktech** &gt; **Společné** &gt; **Modely konfigurace produktu**.
2.  Vyberte model konfigurace produktu a klepněte na panelu akcí na **Upravit**.
3.  Na stránce **Podrobnosti modelu produktu s konfigurací založenou na omezeních** vyberte atribut, který má být použit jako cílový atribut.
4.  Na pevné záložce **Atributy** vyberte **Skrytý** nebo **Jen pro čtení**.

## <a name="can-a-calculation-overwrite-the-values-that-i-set"></a>Může výpočet hodnoty přepsat mnou nastavené hodnoty?
Č. Hodnoty, které jste nastavili při konfiguraci produktu, jsou hodnoty, které budou použity. Výpočet, ke kterému dochází při změně vstupních hodnot ve výpočtu, nemůže přepsat hodnoty, které zadáte pro konkrétní atribut.

## <a name="what-happens-if-i-remove-an-input-value-in-a-calculation"></a>Co se stane, odeberu-li vstupní hodnotu ve výpočtu?
Pokud odeberete vstupní hodnotu ve výpočtu, hodnota cílového atributu je rovněž odebrána.

## <a name="why-do-i-receive-an-error-message-that-says-that-my-model-is-in-contradiction"></a>Proč se zobrazila chybová zpráva s upozorněním, že tento model je v rozporu?
Tato zpráva se zobrazí, když výpočet obsahuje chybu nebo v jedné nebo více omezeních existuje rozpor. Další informace o rozporech v omezeních viz [Omezení výrazu a omezení tabulky](expression-constraints-table-constraints-product-configuration-models.md). Zde jsou uvedeny situace, kdy může dojít k chybám ve výpočtu:

-   Hodnota je dělena nulou.
-   Došlo ke konfliktu mezi těmito dvěma prvky:
    -   Hodnoty, které jsou k dispozici pro atribut a které jsou vymezeny omezením.
    -   Hodnota, která je generována výpočtem.
-   Hodnoty, které jsou vráceny výpočem, jsou mimo doménu atributu. Například celé číslo z \[1..10\], které je vypočítáno na hodnotu 0.

## <a name="why-do-i-receive-an-error-message-even-though-i-successfully-validated-my-product-model"></a>Proč se zobrazila chybová zpráva i v případě, že tento model výrobku byl úspěšně ověřen?
Výpočty nejsou zahrnuty do ověření. Je nutné vyzkoušet model konfigurace produktu pro nalezení chyb při výpočtech. Následující postup umožňuje otestovat model konfigurace produktu.

1.  Klikněte na **Řízení informací o produktech** &gt; **Společné** &gt; **Modely konfigurace produktu**.
2.  Vyberte model konfigurace produktu a klepněte na panelu akcí ve skupině **Spustit** klikněte na **Test**.





