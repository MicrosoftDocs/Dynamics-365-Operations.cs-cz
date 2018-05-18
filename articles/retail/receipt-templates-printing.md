---
title: "Šablony pro příjemky a tisk"
description: "Tento článek popisuje, jak můžete upravovat rozvržení formulářů a určovat tak, jak se mají tisknout účtenky, faktury a další doklady. Microsoft Dynamics 365 for Retail obsahuje návrháře rozvržení formulářů, který umožňuje snadné vytváření a úpravu různých druhů rozvržení formulářů."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFormLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 57841
ms.assetid: e530dd8e-95e2-4021-90bd-ce1235f9e250
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 76cc7f873b99874ef6f2c4bc2ebc3f87fa065647
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="receipt-templates-and-printing"></a>Šablony pro příjemky a tisk

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak můžete upravovat rozvržení formulářů a určovat tak, jak se mají tisknout účtenky, faktury a další doklady. Microsoft Dynamics 365 for Retail obsahuje návrháře rozvržení formulářů, který umožňuje snadné vytváření a úpravu různých druhů rozvržení formulářů.

**Důležité:** Musíte nastavit rozvržení formulářů a profily příjemek, chcete-li tisknout příjemky a další dokumenty z oderních obchodních POS a cloudových POS. Můžete zahrnout více rozložení formuláře do profilu účtenky. Můžete pak přiřadit profil účtenky k tiskárně úpravou profilu hardwaru.

## <a name="set-up-a-receipt-format"></a>Nastavení formátu příjemky
1.  Klepněte na tlačítko **Retail** &gt; **Nastavení kanálu** &gt; **Nastavení POS** &gt; **POS** &gt; **Formáty příjemky**.
2.  Na stránce **Formát příjemky** kliknutím na tlačítko **Nový** vytvořte nové rozvržení formuláře nebo vyberte stávající rozvržení formuláře.
3.  V poli **Formát příjemky** zadejte identifikátor pro rozložení formuláře a vyberte druh příjemky používaný pro toto rozvržení. Můžete také zadat popis a krátký název příjemky v poli **Titul**.
4.  Na pevné záložce **Hlavní** vyberte jednu z možností pro definování chování tisku:
    -   **Vždy vytisknout** – příjemky se vytisknou automaticky podle potřeby.
    -   **Netisknout** – účtenky se nebudou tisknout.
    -   **Vyzvat uživatele** – uživatel je vyzván k vytisknutí účtenky.
    -   **Podle potřeby** – tato možnost slouží pouze pro dárkové příjemky. Pokud je vybrána tato možnost, uživatel může vytisknout dárkovou příjemku ze stránky **Změny**, je-li požadována příjemka k dárku.

## <a name="design-a-receipt-format"></a>Navrhnout formát příjemky
Použijte návrháře rozvržení formuláře ke grafickému vytvoření rozvržení dokumentu formuláře. Stránka **Návrhář formátu příjemky** obsahuje tři oddíly: **Záhlaví**, **Řádky** a **Zápatí**. Některé typy rozvržení formuláře používají prvky ze všech tří oddílů, zatímco jiné typy používají prvky pouze z jednoho nebo dvou oddílů. Chcete-li zobrazit prvky, které jsou k dispozici pro každý oddíl, klikněte na příslušné tlačítko v navigačním podokně na levé straně stránky.

1.  Klepněte na tlačítko **Retail** &gt; **Nastavení kanálu** &gt; **Nastavení POS** &gt; **POS** &gt; **Formáty příjemky**.
2.  Na stránce **Formát příjemky** vyberte rozvržení formuláře a klepněte na tlačítko **Návrhář**.
3.  Klepnutím na tlačítko **Spustit** zahájíte instalaci hostitele maloobchodního návrháře.
4.  Na panelu Oznámení, který se zobrazí v dolní části okna Internet Explorer klepněte na tlačítko **Otevřít** a spusťte tak instalaci předdefinovaného návrháře. (Oznamovací pruh se může zobrazit v jiném umístění v jiných prohlížečích). Indikátor průběhu ukazuje průběh procesu instalace.
5.  Po dokončení instalace zadejte uživatelské jméno a heslo aplikace Dynamics 365 for Retail a klepněte na tlačítko **Přihlásit** pro spuštění návrháře.
6.  Po ověření pověření a spuštění návrháře můžete začít navrhovat formát příjemky nebo změnit existující formát.
7.  Chcete-li vytvořit prvky formuláře, vyberte oddíl **Záhlaví**, **Řádky** nebo **Zápatí** a potom přetáhněte prvek z oddílu do pracovního prostoru. Většina prvků obsahuje proměnné, které jsou automaticky vyplněny daty z databáze. Další prvky, jako **Text**, vám umožňují vytisknout vlastní text na příjemce. **Poznámka:** Změnou čísla v pravém dolním rohu oddílu můžete určit, kolik řádků budou jednotlivé oddíly zabírat. Úpravu oddílu lze usnadnit tak, že zvětšíte výšku daného oddílu přetažením ukazatele velikosti ve spodní části oddílu. Výška oddílu v pracovním prostoru nemá vliv na počet řádků na skutečné příjemce.
8.  Po přetažení prvku do pracovního prostoru nastavte vlastnosti oddílu v podokně **Informace o objektu** v dolní části stránky. Zadejte jedno nebo více z následujících nastavení:
    -   **Zarovnat** – Nastavte zarovnání pole **Vlevo** nebo **Vpravo**.
    -   **Výplňový znak** – Zadejte prázdný znak. Standardně se používá prázdné místo, ale můžete zadat libovolný znak.
    -   **Předpona** – Zadejte hodnotu, která se bude zobrazovat na začátku pole. Toto nastavení se používá pouze v součásti **Řádky** v rámci rozvržení.
    -   **Znaky** – zadejte maximální počet znaků, které pole může obsahovat, pokud prvek obsahuje proměnnou. Pokud je text v poli delší než zadaný počet znaků, bude text zkrácen podle pole.
    -   **Proměnná** – Toto políčko se vybere automaticky, pokud je prvek proměnná a nelze jej přizpůsobit.
    -   **Typ písma** – Nastavte typ písma na **Běžné** nebo **Tučné**. Tučná písmena zabírají dvakrát tolik místa jako běžná písmena. Proto může dojít ke zkrácení některých znaků.
    -   **Velikost písma** – Nastavte velikost písma na **Běžné** nebo **Tučné**. Velká písmena jsou dvakrát větší než běžná písmena. Proto může použití velkých písmen způsobit překrývání textu v příjemce.
    -   **Odstranit** – na toto tlačítko klikněte v případě, že chcete odebrat vybranou součást z rozvržení formuláře.

## <a name="assign-receipt-profiles"></a>Přiřazení profilů účtenek
Profily účtenky jsou přiřazeny přímo k tiskárnám prostřednictvím profilu hardwaru.

1.  Profil hardwaru otevřete klepnutím na tlačítko **Maloobchodní prodej** &gt; **Nastavení kanálu** &gt; **Nastavení POS** &gt; **Profily POS** &gt; **Hardwarový profil**.
2.  Vyberte tiskárnu a poté v poli **Profil účtenky** můžete přiřadit profil účtenky, který chcete použít v pokladně.

**Poznámka:** Pokud jsou použity dvě tiskárny, jednu tiskárnu lze nastavit na tisk standardních termálních účtenek se 40 sloupci. Druhá tiskárna se obvykle používá pro tisk účtenek na celou stránku, které vyžadují další informace. Tyto typy účtenky zahrnují účtenky za objednávky odběratelů a faktury odběratelům.




