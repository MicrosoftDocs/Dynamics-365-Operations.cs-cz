---
title: "Konfigurace a práce s blokováním objednávek kontaktního střediska"
description: "Toto téma popisuje, jak pracovat s blokováním objednávek pomocí aplikace Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 05/14/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: MCRHoldCodeTable, MCRSalesTableOrderHistory, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: ba8fade84358c960dcfd1e8d9ffef1ffede34871
ms.contentlocale: cs-cz
ms.lasthandoff: 01/04/2019

---

# <a name="configure-and-work-with-call-center-order-holds"></a>Konfigurace a práce s blokováním objednávek kontaktního střediska

[!include [banner](includes/banner.md)]

Toto téma popisuje funkce blokování objednávky, které má aplikace Microsoft Dynamics 365 for Retail pro objednávky kontaktního střediska

## <a name="configuring-call-center-order-holds"></a>Konfigurace blokování objednávek kontaktního střediska

Chcete-li použít funkce blokování objednávek kontaktního střediska, je nutné nejprve definovat kódy blokování. Chcete-li vytvořit sadu uživatelem definovaných kódů blokování podle svých obchodních potřeb, přejděte na **Prodej a marketing** \> **Nastavení** \> **Prodejní objednávky** \> **Kódy blokování objednávky**. Můžete nepovinně označit některý z kódů blokování jako výchozí nastavením možnosti **Výchozí pro prodejní objednávku** na **Ano**. Tento kód blokování se použije pokaždé, když je prodejní objednávka blokována. Prodejní objednávka má rezervované zásoby a rezervace musí být automaticky odebrány, pokud je objednávka blokována z určitého důvodu, nastavte možnost **Odebrat rezervace zásob** na **Ano** pro kódy důvodů.

Chcete-li určit typ poznámky, která bude zaznamenána, když uživatelé blokující prodejní objednávku zadají volitelnou poznámku, přejděte na **Pohledávky** \> **Nastavení** \> **Parametry pohledávek**, a poté na pevné záložce **Nastavení prodeje** na kartě **Obecné** nastavte pole **Typ poznámky**. Použijte pole **Stav prodejní objednávky Blokováno** pro definování barvy, která se použije ke zvýraznění prodejních objednávek, které jsou blokovány, pokud jsou zobrazeny na stránce **Odběratelský servis**.

Chcete-li vytvořit volitelnou sadu kódů důvodů blokování, přejděte na **Maloobchod** \> **Nastavení kanálu** \> **Informační kódy**. Tyto informační kódy lze použít jako sekundární kód důvodu pro další definování hlavního kódu blokování. Vyberte **Nový** a vytvořte sadu kódů důvodu, a pak vyberte **Subkódy** k definování seznamu dalších důvodů. Chcete-li propojit všechny informační kódy , které jste definovali pro kanál kontaktního střediska, přejděte na **Maloobchod** \> **Kanály** \> **Kontaktní střediska** \> **Všechna kontaktní střediska**. Na pevné záložce **Obecné** nastavte pole **Kód blokování**.

## <a name="putting-orders-on-hold"></a>Zablokování objednávek

Objednávky, které uživatelé kontaktního střediska vytvoří v programu Retail, lze v konkrétních situacích zablokovat buď ručně nebo automaticky.

Při zadávání objednávky, ale před jejím odesláním a potvrzení, uživatelé kontaktního střediska mohou chtít zablokovat objednávku ručně, aby zabránili jejímu uvolnění do skladu pro další zpracování. Například odběratel, který učiní objednávku, nemusí být připraven se k ní zavázat, nebo mohou chybět důležitá data požadovaná ke zpracování objednávky.

Na stránce zadání objednávky může uživatel kontaktního střediska zablokovat objednávku s použitím možnost **Blokování objednávky** na kartě **Prodejní objednávka** nabídky zadání objednávky. Popřípadě může uživatel vybrat položku nabídky **Blokování** na stránce **Souhrn prodejní objednávky**, která se zobrazí po volbě **Dokončit** na prodejní objednávce kontaktního střediska.

V obou případech se zobrazí stránka **Blokování objednávky**. Uživatel pak může vybrat **Nový** pro vytvoření blokování objednávky. V poli **Kód blokování**, uživatel musí zvolit kód, který nejlépe popisuje důvod blokování. V poli **Kód důvodu** uživatel může volitelně vybrat další kód, aby zadal druhou úroveň popisu blokování.

Na pevné záložce **Poznámky** v poli **Poznámky blokování** uživatel můžete zadat další volné poznámky k poskytnutí dalšího kontextu nebo informací o blokování. Tyto poznámky mohou pomoct ostatním uživatelům, kteří kontrolují nebo pracují s blokováním objednávky později.

Po zadání a uložení informace o blokování může uživatele zavřít stránku **Blokování objednávek**. Uživatel se poté vrátí na stránku zadávání prodejní objednávky. Jestliže nejsou požadovány žádné další akce k prodejní objednávce, může uživatele zavřít stránku zadávání prodejní objednávky.

Pokud je příznak **Povolit dokončení objednávky** zapnutý v kanálu kontaktního střediska, platba nemusí být použita na objednávku, která je blokována. Naproti tomu, pro prodejní objednávku, která není blokována, uživatelé nemohou opustit stránku zadávání prodejní objednávky, dokud není platba aplikována. Samozřejmě bude vyžadována platba před uvolněním blokování objednávky.

Dále mohou uživatelé kontaktního střediska provést manuální blokování proti podvodu na objednávkách , které jsou z nějakého důvodu podezřelé. Objednávky lze rovněž blokovat automaticky, pokud naplní aktivní kritéria a pravidla podvodu. Další informace o tomto typu blokování objednávky naleznete v tématu [Nastavení výstrah u podvodů](https://docs.microsoft.com/dynamics365/unified-operations/retail/set-up-fraud-alerts).

## <a name="viewing-and-managing-orders-that-are-on-hold"></a>Zobrazení a správa objednávek, které jsou blokované

### <a name="viewing-hold-information-for-a-single-sales-order"></a>Zobrazení informací o blokování pro jednu prodejní objednávku

Na stránce **Odběratelský servis** mohou uživatelé vizuálně určit objednávky, které jsou blokované, protože řádky objednávky jsou zvýrazněny určitou barvou. Tato barva je definována polem **Stav prodejní objednávky Blokováno** na stránce **Parametry pohledávek**.

> [!NOTE]
> Pokud je řádek na stránce zvolen, barva zvýraznění není viditelná.

Uživatelé mohou také zobrazit podrobné informace o stavu pro prodejní objednávku, chtějí-li zjistit, zda je objednávka blokována. Podrobné informace o stavu lze otevřít ze stránek **Všechny prodejní objednávky** nebo **Odběratelský servis**. Pokud je objednávka blokována, je pro ní nastaven příznak **Nezpracovávat** a pole **Podrobný stav** ukazuje stav buď **Blokováno** nebo **Blokování podvodu** podle scénáře.

Chcete-li zobrazit podrobnosti individuálního blokování objednávky, mohou uživatelé otevřít podrobné zobrazení stránky **Blokování objednávky** ze stránky **Odběratelský servis** pomocí nabídky **Možnosti** pro vybranou objednávku. Uživatelé se mohou rovněž dostat na toto zobrazení ze stránky **všechny prodejní objednávky** výběrem položky nabídky **Blokování objednávky** na kartě **Prodejní objednávka**.

### <a name="viewing-all-orders-that-are-on-hold"></a>Zobrazení všech objednávek, které jsou blokované

Chcete-li zobrazit všechny objednávky, které byly ručně nebo automaticky zablokovány, přejděte na **Maloobchod** \> **Odběratelé** \> **Blokování objednávek**.

Pracovní plocha **Blokování objednávek** obsahuje zobrazení seznamu všech objednávek, které jsou blokovány kvůli akcím ručního blokování nebo blokování proti podvodu. Využitím standardních možností filtrování a třídění na stránce mohou uživatelé mohou vytvářet zobrazení, která jim umožňují pracovat s určitými kódy blokování, nebo je spravovat, u nichž jsou zodpovědní za jejich kontrolu. Pracovní plocha **Blokování objednávek** také označuje počet dní, po které byla objednávka blokována. Tyto informace mohou pomoci uživatelům určit prioritu fronty.

Chcete-li získat podrobnější zobrazení objednávek, které jsou blokované, mohou uživatelé kliknout na možnost **Blokování objednávky** z nabídky. Toto zobrazení poskytuje informace o odběrateli poznámky, které byly použity pro objednávky, odběratele nebo akce blokování. Zobrazení také nabízí podrobnosti o důvodu automatického blokování, pokud byla objednávka blokována proto, že splňuje kritéria pravidla podvodu.

Ze zobrazení seznamu i z podrobného zobrazení stránky **Blokování objednávky** mohou uživatelé zobrazit nebo upravit další informace související s objednávkou, například platby, součty a poznámky.

Možnosti na kartě **Rezervace blokování** mohou být užitečné tehdy, když více uživatelů ve vaší společnosti pracuje ve frontě blokování současně. Výběrem možnosti **Rezervovat** mohou uživatelé určit, že pracují na revizi a zkoumání blokování objednávky. Tímto způsobem ostatní uživatelé nebudou ztrácet čas stejnou prací. Z podrobného zobrazení stránky **Blokování objednávky** uživatelé mohou zobrazit informace o datu a času rezervace, a o tom, který uživatel si rezervoval záznam blokování.

Poté, co je záznam blokování rezervován, může pouze uživatel, který rezervaci provedl, tuto rezervaci zrušit. Toto omezení má zabránit uživatelům dělat záznamy, na kterých již pracují jiní uživatelé. Chcete-li uvolnit objednávku zpět do fronty, aby na ní ostatní uživatelé mohli pracovat, uživatel, který provedl rezervaci, zvolí možnost **Vymazat rezervaci**.

> [!NOTE]
> Blokování není uvolněno, když je rezervace vymazána.

V některých situacích, například když je uživatel nemocný nebo opustil společnost, záznamy, které jsou rezervovány pro daného uživatele, musí být přiřazeny jinému uživateli. Manažer může změnit přiřazení záznamů s použitím možnosti **Přepsat rezervaci**.

## <a name="releasing-orders-that-are-on-hold"></a>Uvolnění objednávek, které jsou blokované

V zobrazení seznamu a podrobném zobrazení stránky **Blokování objednávky** obsahuje karta **Vymazat blokování** možnosti, které slouží k uvolnění blokování objednávky. Použijte možnost **Vymazat blokování** k uvolnění objednávky z vybraného kódu blokování.

Objednávky kontaktního střediska vyžadují platbu. Proto nelze blokování vymazat úplně, pokud objednávka nebyla ještě zaplacena. Na stránce **Parametry kontaktního střediska** na kartě **Blokování** se ujistěte, že parametr **Odeslat při vymazání** je zapnutý. Toto nastavení pomáhá zajistit, že objednávka s vymazaným blokováním projde správnou logikou odeslání objednávky k ověření a autorizaci plateb. Pokud platby chybí, obdrží uživatel chybu a kód blokování se neodstraní.

Pokud nebyl parametr **Odeslat při vymazání** nastaven, uživatelé by měli zvolit možnost **Vymazat a odeslat** v nabídce **Vymazat blokování** k zajištění, že objednávka projde všemi požadovanými ověřeními platby. Pokud se odeslání objednávky nezdaří, když je příznak **Povolit dokončení objednávky** zapnutý na kanálu kontaktního střediska, uvolnění se stav blokování z objednávky, ale příznak **Nezpracovávat** zůstane nastavený. Proto není objednávka uvolněna do skladu, dokud nebyly použity a ověřeny správné platby.

Pokud uživatelé chtějí vymazat blokování a provést ještě další změny objednávky před jejím uvolněním k dalšímu zpracování, mohou vybrat možnost **Vymazat a upravit**. Tato možnosti odebere kód blokování a otevře podrobnosti prodejní objednávky tak, aby uživatelé mohli provádět další změny objednávky. Uživatelé mohou také použít platby a odeslat prodejní objednávku pomocí logiku ověřování platby, když je příznak **Povolit dokončení objednávky** zapnutý na kanálu kontaktního střediska.

## <a name="reporting-options"></a>Možnosti vykazování

Přejděte na **Maloobchod** \> **Dotazy a sestavy** \> **Sestavy kontaktního střediska** \> **Sestavy blokování objednávky** a spusťte sestavu týkající se blokování objednávek podle rozsahu dat, kódu blokování nebo jiných souvisejících kritérií.

