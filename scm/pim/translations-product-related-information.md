---
title: "Související produkt překladů FAQ"
description: "Toto téma popisuje, jak spravovat překlady pro produkty, hodnoty dimenze produktu a atributy produktu."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysTranslationDetail, SysTranslationLanguage, SysTranslationList
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 201853
ms.assetid: c0286bba-f54b-42de-904c-81fd796bdd1d
ms.search.region: global
ms.search.industry: Product information
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: a9c991a5afaebd10b8812dfc1d67120ed4ebdfd2
ms.lasthandoff: 03/31/2017


---

# <a name="product-related-translations-faq"></a>Související produkt překladů FAQ

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

## <a name="how-do-i-create-translations-for-productrelated-information"></a>Vytvoření překladů pro informace productrelated
Při vytváření překladů produktu postupujte takto:
1.  Klepněte na tlačítko **řízení informací o produktech**&gt;**běžné**&gt;**uvolněných produktů**.
2.  Vyberte produkt a v podokně akcí v **jazyky** skupinu, klepněte na tlačítko **překlady**.
3.  Na stránce **Překlad textu** v poli **Jazyk** vyberte jazyk. Chcete-li přidat další jazyky, rozbalte **jazyka** pole a potom klepněte na tlačítko **OK**.
4.  Ve skupině **Přeložený text** Zadejte překlad do polí **Popis** d **Název produktu**.

Při vytváření překladů atributů produktu postupujte takto:
1.  Klepněte na tlačítko **řízení informací o produktech**&gt;**běžné**&gt;**uvolněných produktů**.
2.  Ve skupinovém rámečku **Nastavení** klepněte na tlačítko **Atributy** a klepněte na tlačítko **Atributy**.
3.  Na stránce **Atributy** klepněte na **Přeložit**.
4.  Na stránce **Překlad textu** v poli **Jazyk** vyberte jazyk. Chcete-li přidat další jazyky, rozbalte **jazyka** pole a potom klepněte na tlačítko **OK**.
5.  Ve skupině **Přeložený text** napište překlady do polí **Popis**, **Popisný název** a **Text nápovědy**.

Při vytváření překladů hodnot dimenze produktu postupujte takto:
1.  Klepněte na tlačítko **řízení informací o produktech**&gt;**běžné**&gt;**uvolněných produktů**.
2.  Vyberte produkt a klepněte na možnost **Rozměry produktu**.
3.  Vyberte jeden z odkazů pro dimenze produktu: **Konfigurace**, **Velikosti**, **Barvy** nebo **Styl**.
4.  Vyberte hodnotu dimenze a poté klikněte na položku **Přeložit**.
5.  Na stránce **Překlad textu** v poli **Jazyk** vyberte jazyk. Chcete-li přidat další jazyky, rozbalte **jazyka** pole a potom klepněte na tlačítko **OK**.
6.  V **přeložený text** skupinu, zadejte překlady v **jméno** a **popis** pole.

## <a name="can-the-names-of-product-variants-be-translated"></a>Je možné přeložit názvy variant produktu?
Varianty produktu, které jsou založené na dimenzích vydaného produktu. Názvy variant produktu jsou založeny na kombinaci hodnot dimenzí. Pokud jsou přeloženy hodnoty dimenze, které jsou přidruženy k variantě produktu, název varianty produktu se zobrazí v přeloženou verzi.  

**Příklad**  

Produkt je tričko dodávané v různých velikostech a barvách a názvy variant jsou založeny na následujících údajích:
-   Číslo výrobku: \#3
-   Dimenze: Velikost a barva
-   Hodnoty velikosti dimenze: malá, střední, velká
-   Hodnoty barvy dimenze: červená, zelená, černá

Malé hodnoty název varianty produktu, který je založen na dimenzi a červená barva je **\#3:Small:Red**.  

Zákazník chce koupit nějaká malá červená trička a název tričko musí být na faktuře ve francouzštině. Převést hodnoty dimenze malá a červená, do francouzštiny a název varianty produktu je **\#3: Petit: Rouge**.
<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Tip </strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Pokud chcete nastavit upřednostňovaný jazyk odběratele, postupujte takto:
<ol>  
<li>Klepněte na tlačítko <strong>prodeje a marketingu</strong>&gt;<strong>běžné</strong>&gt;<strong>zákazníci</strong>&gt;<strong>všechny</strong> <strong>zákazníci</strong>.</li>
<li>Kliknutím dvakrát na účet odběratele otevřete formulář <strong>Zákazníci</strong>. Na kartě <strong>Obecné</strong> vyberte v poli <strong>Jazyk</strong> požadovaný <strong>jazyk</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="what-happens-if-a-customer-has-a-preferred-language-for-which-no-translations-are-available"></a>Co se stane, pokud má odběratel preferovaný jazyk, pro který není k dispozici žádný překlad?
Pokud pro upřednostňovaný jazyk odběratele nejsou k dispozici překlady, názvy a popisy se zobrazují v globálním jazyce vaší vlastní společnosti.

## <a name="can-i-manage-translations-for-a-series-of-dimension-values-at-the-same-time"></a>Lze spravovat současně překlady pro celou řadu hodnot dimenzí?
Hodnoty dimenzí jsou specifické pro produkt a můžete spravovat překlady hodnot dimenzí pro každý výrobek. Pokud ale vytvoříte skupinu hodnot dimenze a přeložíte hodnoty ve skupině hodnot, je správa překladů jednodušší.   

**Example**  

Společnost vyrábí trička v různých stylech a všechny jsou dostupné ve velikostech Malá, Střední a Velká. Velikosti jsou shromážděny v jedné skupině hodnot dimenzí. Když je přidán nový styl trička, můžete jej přidružit ke skupině hodnot dimenze, která se použije pro velikosti, tak, aby všechny velikosti byly k dispozici pro produkt. Můžete také kdykoli přidat nebo změnit překlady velikostí ve skupině hodnot dimenzí.  

Hodnota dimenze přiřazená k produktu prostřednictvím skupiny variant dimenzí musí být spravovaná ze skupiny variant produktu.   
Pokud chcete vytvořit skupinu pro hodnotu dimenze, postupujte takto:
1.  Klepněte na tlačítko **řízení informací o produktech**&gt;**nastavení**&gt;**skupiny Variant**.
2.  Vyberte **Skupiny** **velikostí**, **Skupiny barev** nebo **Skupiny stylů**.
3.  Klepněte na tlačítko **nové**a poté zadejte název skupiny v **velikost****skupiny**, **skupinu barev**, nebo **skupinu stylů** pole. Kliknutím na **Velikosti**, **Barvy** nebo **Styly** vytvořte řádky pro skupiny.
4.  V **velikost****skupiny** řádky, **barva****skupiny****řádky**, nebo **řádky skupiny stylů** klepněte na tlačítko **nový**a pak vytvořte velikosti, barvy a styly pro skupiny.

Pokud chcete spravovat překlady hodnot v určité skupině hodnot dimenze, postupujte takto:
1.  Postupujte podle pokynů v předchozím postupu pro vytvoření skupiny hodnot dimenzí k otevření stránky **Řádky skupiny velikostí**, **Řádky skupiny barev**, nebo **Řádky skupiny stylů**.
2.  Klikněte na **Překlad textu**. V **překlad textu** stránky v **přeložený text** skupinu, zadejte překlady v **jméno** a **popis** pole.

## <a name="when-can-translations-of-productrelated-information-be-managed"></a>Kdy lze spravovat překlady productrelated informace?
Překlady informací souvisejících s produktem lze spravovat kdykoli. Při aktualizaci překladů pro hodnotu dimenze, která je přidružena k produktu, se aktualizují informace o produktu, bez ohledu na to, zda má produkt transakce.






