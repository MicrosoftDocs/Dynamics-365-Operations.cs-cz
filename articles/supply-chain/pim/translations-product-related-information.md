---
title: "Překlady související s produktem – nejčastější dotazy"
description: "Toto téma popisuje, jak spravovat překlady pro produkty, hodnoty dimenze produktu a atributy produktu."
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysTranslationDetail, SysTranslationLanguage, SysTranslationList
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 201853
ms.assetid: c0286bba-f54b-42de-904c-81fd796bdd1d
ms.search.region: global
ms.search.industry: Product information
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 87dfdf7085e185b3e0467088118838eb832546d7
ms.contentlocale: cs-cz
ms.lasthandoff: 02/07/2018

---

# <a name="product-related-translations-faq"></a>Překlady související s produktem – nejčastější dotazy

[!include[banner](../includes/banner.md)]


Toto téma popisuje, jak spravovat překlady pro produkty, hodnoty dimenze produktu a atributy produktu. 

<a name="what-product-related-data-can-be-translated"></a>Jaká data související s produktem lze přeložit?
--------------------------------------------

Můžete vytvářet překlady následujících informací souvisejících s produkty:
-   Názvy a popisy produktů.
-   Popisy, popisné názvy a text nápovědy hodnot atributů produktu.
-   Názvy a popisy hodnot dimenze produktu

Informace související s produkty můžete překládat do jakéhokoli jazyka, který je k dispozici ze stránky **Překlad textu**. Další informace naleznete v následující části **Vytvoření překladů pro informace související s produktem**.

## <a name="where-can-i-view-the-translated-information"></a>Kde se můžu podívat na přeložené informace?
Překlad informací o produktu můžete zobrazit v jakémkoli externím zdrojovém dokumentu, jako je faktura, která používá jazyk, kde jsou k dispozici překlady.

## <a name="how-do-i-create-translations-for-product-related-information"></a>Další informace naleznete v tématu Vytvoření překladů pro informace související s produktem.
Při vytváření překladů produktu postupujte takto:
1.  Klikněte na **Řízení informací o produktech** &gt; **Společné** &gt; **Uvolněné produkty**.
2.  Vyberte produkt a v podokně akcí ve skupině **Jazyky** klikněte na **Překlady**.
3.  Na stránce **Překlad textu** v poli **Jazyk** vyberte jazyk. Pokud chcete přidat více jazyků, rozbalte pole **Jazyk** a klikněte na **OK**.
4.  Ve skupině **Přeložený text** Zadejte překlad do polí **Popis** d **Název produktu**.

Při vytváření překladů atributů produktu postupujte takto:
1.  Klikněte na **Řízení informací o produktech** &gt; **Společné** &gt; **Uvolněné produkty**.
2.  Ve skupinovém rámečku **Nastavení** klepněte na tlačítko **Atributy** a klepněte na tlačítko **Atributy**.
3.  Na stránce **Atributy** klepněte na **Přeložit**.
4.  Na stránce **Překlad textu** v poli **Jazyk** vyberte jazyk. Pokud chcete přidat více jazyků, rozbalte pole **Jazyk** a klikněte na **OK**.
5.  Ve skupině **Přeložený text** napište překlady do polí **Popis**, **Popisný název** a **Text nápovědy**.

Při vytváření překladů hodnot dimenze produktu postupujte takto:
1.  Klikněte na **Řízení informací o produktech** &gt; **Společné** &gt; **Uvolněné produkty**.
2.  Vyberte produkt a klepněte na možnost **Rozměry produktu**.
3.  Vyberte jeden z odkazů pro dimenze produktu: **Konfigurace**, **Velikosti**, **Barvy** nebo **Styl**.
4.  Vyberte hodnotu dimenze a poté klikněte na položku **Přeložit**.
5.  Na stránce **Překlad textu** v poli **Jazyk** vyberte jazyk. Pokud chcete přidat více jazyků, rozbalte pole **Jazyk** a klikněte na **OK**.
6.  Ve skupině **Přeložený text** zadejte překlady do polí **Název** a **Popis**.

## <a name="can-the-names-of-product-variants-be-translated"></a>Je možné přeložit názvy variant produktu?
Varianty produktu, které jsou založené na dimenzích vydaného produktu. Názvy variant produktu jsou založeny na kombinaci hodnot dimenzí. Pokud jsou přeloženy hodnoty dimenze, které jsou přidruženy k variantě produktu, název varianty produktu se zobrazí v přeloženou verzi.  

**Příklad**  

Produkt je tričko dodávané v různých velikostech a barvách a názvy variant jsou založeny na následujících údajích:
-   Číslo produktu: \#3
-   Dimenze: Velikost a barva
-   Hodnoty velikosti dimenze: malá, střední, velká
-   Hodnoty barvy dimenze: červená, zelená, černá

Název varianty produktu, která je založená na hodnotách dimenze Malá a Červená, je **\#3:Malá:Červená**.  

Zákazník chce koupit nějaká malá červená trička a název tričko musí být na faktuře ve francouzštině. Přeložíte hodnoty dimenze Malá a Červená do francouzštiny a název varianty produktu je **\#3:Petit:Rouge**.
<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Tip</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Pokud chcete nastavit upřednostňovaný jazyk odběratele, postupujte takto:
<ol>  
<li>Klikněte na <strong>Prodej a marketing</strong> &gt; <strong>Společné</strong> &gt; <strong>Zákazníci</strong> &gt; <strong>Všichni</strong> <strong>zákazníci</strong>.</li>
<li>Kliknutím dvakrát na účet odběratele otevřete formulář <strong>Zákazníci</strong>. Na kartě <strong>Obecné</strong> vyberte v poli <strong>Jazyk</strong> požadovaný <strong>jazyk</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="what-happens-if-a-customer-has-a-preferred-language-for-which-no-translations-are-available"></a>Co se stane, pokud má odběratel preferovaný jazyk, pro který není k dispozici žádný překlad?
Pokud pro upřednostňovaný jazyk odběratele nejsou k dispozici překlady, názvy a popisy se zobrazují v globálním jazyce vaší vlastní společnosti.

## <a name="can-i-manage-translations-for-a-series-of-dimension-values-at-the-same-time"></a>Lze spravovat současně překlady pro celou řadu hodnot dimenzí?
Hodnoty dimenzí jsou specifické pro produkt a můžete spravovat překlady hodnot dimenzí pro každý výrobek. Pokud ale vytvoříte skupinu hodnot dimenze a přeložíte hodnoty ve skupině hodnot, je správa překladů jednodušší.   

**Příklad**  

Společnost vyrábí trička v různých stylech a všechny jsou dostupné ve velikostech Malá, Střední a Velká. Velikosti jsou shromážděny v jedné skupině hodnot dimenzí. Když je přidán nový styl trička, můžete jej přidružit ke skupině hodnot dimenze, která se použije pro velikosti, tak, aby všechny velikosti byly k dispozici pro produkt. Můžete také kdykoli přidat nebo změnit překlady velikostí ve skupině hodnot dimenzí.  

Hodnota dimenze přiřazená k produktu prostřednictvím skupiny variant dimenzí musí být spravovaná ze skupiny variant produktu.   
Pokud chcete vytvořit skupinu pro hodnotu dimenze, postupujte takto:
1.  Klepněte na tlačítko **Řízení informací o produktech** &gt; **Nastavení** &gt; **Skupiny variant**.
2.  Vyberte **Skupiny** **velikostí**, **Skupiny barev** nebo **Skupiny stylů**.
3.  Klepněte na tlačítko **Nový** a poté zadejte název skupiny do pole **Skupina** **velikostí**, **Skupina barev** nebo **Skupina stylů**. Kliknutím na **Velikosti**, **Barvy** nebo **Styly** vytvořte řádky pro skupiny.
4.  Na stránce řádků **Skupina** **velikostí**, **Řádky** **skupiny** **barev** nebo **Řádky skupiny stylů** klikněte na **Nový** a vytvořte velikosti, barvy a styly skupin.

Pokud chcete spravovat překlady hodnot v určité skupině hodnot dimenze, postupujte takto:
1.  Postupujte podle pokynů v předchozím postupu pro vytvoření skupiny hodnot dimenzí k otevření stránky **Řádky skupiny velikostí**, **Řádky skupiny barev**, nebo **Řádky skupiny stylů**.
2.  Klikněte na **Překlad textu**. Na stránce **Překlad textu** ve skupině **Přeložený text** zadejte překlady do pole **Název** a **Popis**.

## <a name="when-can-translations-of-product-related-information-be-managed"></a>Kdy lze spravovat překlady informací souvisejících s produktem?
Překlady informací souvisejících s produktem lze spravovat kdykoli. Při aktualizaci překladů pro hodnotu dimenze, která je přidružena k produktu, se aktualizují informace o produktu, bez ohledu na to, zda má produkt transakce.






