---
title: "Informace můžete vyhledat pomocí vyhledávání"
description: "Mnoho polí mít 365 Microsoft Dynamics pro operace, vyhledávání, které můžete snadno najít správné nebo požadovanou hodnotu. Několik vylepšení byly přidány do vyhledávání, které tyto ovládací prvky ulehčit a zvýší produktivitu uživatelů. V tomto tématu se dozvíte o těchto nových funkcích vyhledávání a zobrazí některé užitečné tipy pro získání optimálního využití z vyhledávání v systému."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 6a25593632575dcd71fa4a3c9cf5b83c9f8ecd39
ms.lasthandoff: 03/31/2017


---

# <a name="use-lookups-to-find-information"></a>Informace můžete vyhledat pomocí vyhledávání

[!include[banner](../includes/banner.md)]


Mnoho polí mít 365 Microsoft Dynamics pro operace, vyhledávání, které můžete snadno najít správné nebo požadovanou hodnotu. Několik vylepšení byly přidány do vyhledávání, které tyto ovládací prvky ulehčit a zvýší produktivitu uživatelů. V tomto tématu se dozvíte o těchto nových funkcích vyhledávání a zobrazí některé užitečné tipy pro získání optimálního využití z vyhledávání v systému.  

<a name="responsive-lookups"></a>Vyhledávání přestane reagovat
------------------

V předchozích verzích 365 Dynamics pro operace při interakci s vyhledávací ovládací prvek uživatel musel provést explicitní akce chcete-li otevřít rozevírací nabídky. Pravděpodobně se zadáním hvězdičky (\*) k filtrování vyhledávání založené na aktuální hodnotu ovládacího prvku do ovládacího prvku, klikněte na tlačítko rozevíracího seznamu nebo pomocí **Alt**+**šipka dolů** klávesovou zkratku. Vyhledávací ovládací prvky byly změněny s běžnou praxí web lépe přizpůsobit následujícími způsoby:

-   Rozevírací nabídky vyhledávání se otevře automaticky po lehké přerušíte zadávání pomocí rozevíracího seznamu obsahu nabídky filtrovat podle hodnoty vyhledávací ovládací prvek.
    -   Všimněte si, že staré chování automatické otevření rozevíracího seznamu po zadání hvězdičky (\*) se již nepoužívá.
-   Po otevření rozevírací nabídky vyhledávání nastane:
    -   Kurzor zůstane v vyhledávacího prvku (místo fokus přesunout do rozevírací nabídky), můžete i nadále měnit hodnotu ovládacího prvku. Však uživatel může použít **šipka nahoru** a **šipka dolů** změnit řádky v rozevírací nabídce a vyberte v rozevírací nabídce aktuální řádek zadejte.
    -   Po provedení změny hodnoty ovládacího prvku vyhledávání, budou upraveny obsah rozbalovací nabídky.

Zvažte například vyhledávací pole s názvem **Město**. 

Pokud je fokus v **Město** pole, můžete spustit hledáte Město, které má napsáním několika písmen jako "col".  Po ukončení zadávání vyhledávání otevře automaticky filtrovány do těchto měst, které začínají "col". 

[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png) 

V tomto okamžiku kurzor je stále ve vyhledávacím poli. Pokud budete pokračovat v psaní, hodnota je "šířka", vyhledávání obsahu se automaticky upraví tak, aby odrážely nejnovější hodnoty v ovládacím prvku. 

![updateFilterLookupExample](./media/updatefilterlookupexample.png) 

I když stále v vyhledávací ovládací prvek je aktivní, můžete použít také **šipka nahoru** nebo **šipka dolů** klíče, vyberte řádek, který chcete vybrat. Stisknete-li **Enter** zvýrazněný řádek bude vybrán z vyhledávání a zaktualizuje hodnotu ovládacího prvku. 

![changingSelectionLookup](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a>Zadání více než ID
Při zadávání dat, je přirozený pro uživatele, pokus o identifikaci subjektu, například pro zákazníka nebo dodavatele, pokud jde o název, nikoli identifikátor představující entity. V aktuální verzi Dynamics 365 pro operace vyhledávání mnoho (ale ne všechny) nyní umožňují zadání kontextová data. Tato výkonná funkce umožňuje uživateli do ovládacího prvku vyhledávání zadejte odpovídající název nebo Identifikátor. 

Zvažte například **účet odběratele** pole při vytváření prodejní objednávky. Toto pole ukazuje **ID účtu** pro zákazníka, ale uživatel obvykle raději zadat **název účtu** místo **ID účtu** pro toto pole při vytváření prodejní objednávky, například "Doménové struktury Wholesales" místo "USA-003."

Pokud uživatel zahájil vstupovat **ID účtu** do vyhledávacího prvku rozevírací nabídky automaticky otevřou jak je popsáno v předchozí části a uživatel uvidí vyhledávání, jak je ukázáno níže.

[![Kontextové vyhledávání po zadání ID účtu zákazníka](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)

Však lze nyní také zadat začátek **název účtu** také. Pokud je tento zjištěn, uživatel uvidí následující vyhledávání. Oznámení jak na **název** sloupec je přesunuta do vyhledávacího pole v prvním sloupci se a na základě způsobu vyhledávání je seřazeno a filtrováno **název** sloupec.

[![Kontextové vyhledávání po zadání názvu odběratele](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a>Pomocí záhlaví sloupců mřížky pro rozšířené filtrování a řazení
Vylepšení vyhledávání popsané v předchozích dvou částech značně zlepšit schopnost uživatele procházet řádky ve vyhledávání založené na vyhledávání "začíná na" **ID** nebo **jméno** v vyhledávání pole. Existují však situace, ve kterých rozšířené filtrování (nebo řazení) je třeba najít správný řádek. V těchto případech uživatel musí používat v záhlavích sloupců mřížky do vyhledávacího pole možnosti filtrování a řazení. Zvažte například zaměstnance zadávání řádek prodejní objednávky, kdo potřebuje najít pravé "kabel" jako produkt. Psaní do "kabel" **číslo položky** ovládací prvek není vhodné, protože neexistují žádné názvy produktů začínající na "kabel." 

![emptyitemlookup](./media/emptyitemlookup.png) 

Místo toho uživatel musí zrušte hodnotu ovládacího prvku vyhledávání, otevřete rozevírací nabídce vyhledávání a filtrovat rozevírací nabídky pomocí záhlaví sloupce mřížky, jak je ukázáno níže. Myš (nebo dotykem) uživatel může jednoduše klepněte na tlačítko (nebo touch) libovolné záhlaví sloupce, chcete-li získat přístup k filtrování a řazení pro daný sloupec možnosti. Klávesnice uživatele, uživatel potřebuje pouze stiskněte klávesu **Alt**+**dolů****šipka** podruhé přesunout fokus do rozevírací nabídky, po které uživatel může karta do správného sloupce a stiskněte klávesu **Ctrl**+**G** k otevření rozevírací nabídky Mřížka sloupec záhlaví. 

[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png) 

Po použití filtru (viz následující obrázek), můžete uživatele najít a vyberte řádek jako obvykle. 

![filtereditemlookup](./media/filtereditemlookup.png)




