---
title: "Vytvoření kupónů pro maloobchodní prodej"
description: "Toto téma poskytuje přehled maloobchodních kupónů a vysvětluje postup při jejich nastavení."
author: scott-tucker
manager: AnnBe
ms.date: 05/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.custom: 
ms.search.region: Global
ms.search.industry: retail
ms.author: scotttuc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: cebd1b6f041e18c2e016142aba7447bf813f570b
ms.openlocfilehash: fb013d3695870cb3b69ac41ff488f0865a648be4
ms.contentlocale: cs-cz
ms.lasthandoff: 06/19/2017


---

# <a name="create-coupons-for-retail-sales"></a>Vytvoření kupónů pro maloobchodní prodej

[!include[banner](includes/banner.md)]


## <a name="overview-of-coupons"></a>Přehled kupónů

Kupóny jsou kódy a čárové kódy, které slouží k přidání maloobchodních slev do transakce. Každý kupón může mít několik kódů a všechny kódy můžou mít vlastní data účinnosti. 

Každý kupón se vztahuje k jedné maloobchodní slevě. Cenové skupiny, které jsou spojeny se slevou, definují zákazníky, kteří mohou použít kupón nebo kanály, kde je kupón platný. 

Kupóny v zásadě představují další ověření nad rámec maloobchodních slev. Kupón obsahuje kódy kupónu a čárové kódy, které jsou vyžadovány, spolu s rozsahy kalendářních dat pro tyto kódy. Kupón také poskytuje volitelné limity použití a vlastnosti definované zákazníkem. Sleva obsahuje sadu produktů, pro které kupón platný. Cenové skupiny pro slevu poskytují sadu zákazníků, kanálů nebo katalogů, pro které je kupón platný.

Kupón vytvoříte tak, že vytvoříte slevu a kupón samostatně. Pak je spojíte výběrem slevy na stránce kupónu v aplikaci Microsoft Dynamics 365 for Retail. 

> [!NOTE]
> Po té, co je kupón propojen se slevou, několik polí na stránce slevy v aplikaci Microsoft Dynamics 365 for Retail začne být jen pro čtení, vzhledem k tomu, že jsou spravovány nastavením kupónu. Tato pole zahrnují pole pro stav a standardní rozsahy dat.

### <a name="limited-use-coupons"></a>Kupóny s omezeným použitím

Kupóny lze konfigurovat jako kupóny na omezené použití. Limit použití lze definovat na jednoho odběratele nebo kanál nebo jako globální omezení. Toto omezení je vynuceno při zadání kódu nebo čárového kódu nebo naskenování v POS nebo při zadávání prodejní objednávky. Kupón je zaznamenán jako použitý při dokončení objednávky, se kterou je spojený kupón.

Limite je vynucen na kód kupónu v kupónu. Jednorázový kupón, který má dva kódy, lze například použít dvakrát: jednou pro každý kód. Každý kód na kupónu může být nezávisle nastaven na aktivní.

## <a name="managing-coupons"></a>Správa kupónů

Slevu a kupón musíte vytvořit samostatně. Pak je spojíte výběrem slevy na stránce kupónu. Po propojení kupónu se slevou několik polí na stránce slevy začne být jen pro čtení, vzhledem k tomu, že jsou spravována nastavením kupónu. Tato pole zahrnují pole pro stav a standardní rozsahy dat.  

Kupóny v zásadě nyní představují další ověření nad rámec maloobchodních slev. Kupón obsahuje kódy kupónu a čárové kódy, které jsou vyžadovány, spolu s rozsahy kalendářních dat, limity použití a vlastnosti vyžadované zákazníkem. Sleva obsahuje sadu produktů, pro které kupón platný. Cenové skupiny slevy poskytují sadu zákazníků, kanálů nebo katalogů, pro které je kupón platný.

## <a name="system-setup-for-coupons"></a>Nastavení systému pro kupóny 

Před nastavením kupónu je nutné nakonfigurovat čárový kód kupónu a dvě číselné řady kupónu. 

1.  Na stránce **znaky masky** vytvořte nový znak masky pro kód kupónu. Vybrat můžete jakýkoli nepoužitý znak.
2.  Na stránce **Nastavení masky čárového kódu** vytvořte novou masku čárového kódu. Nastavte pole **Typ** na hodnotu **Kupón**.
3.  Na stránce **Nastavení čárového kódu** vytvořte nový čárový kód, který používá právě vytvořenou masku čárového kódu.
4.  Na stránce **Číselné řady** vytvořte dva nové číselné řady. Jedna řada je určena pro ID kódu kupónu a druhá pro číslo kupónu. ID kupónu je jedinečný identifikátor pro každý kód kupónu pro kupón. Číslo kupónu je jedinečný identifikátor kupónu. Každý kupón může mít více kódů a čárových kódů, které ho aktivují.

    > [!NOTE]
    > Pro obě číselné řady je nutné nastavit pole **Obor** na **Společnosti**. Ve většině případů byste měli automaticky generovat obě pořadová čísla.

5.  Na stránce **Sdílené maloobchodní parametry** na kartě **Čárové kódy** vyberte čárový kód, který jste vytvořili dříve.
6.  Na stránce **Parametry maloobchodu** na kartě **číselné řady** vyberte číselné řady, které jste vytvořili pro číslo kupónu a ID kódu kupónu
7.  Nyní můžete otevřít stránku **Kupóny** stránky a vytvořit nové kupóny.

## <a name="the-effect-of-partial-updates-on-coupons"></a>Vliv částečných aktualizací na kupóny

Funkce kupón zahrnuje více různých funkcí v 365 Dynamics for Retail. Maloobchodní centrály aplikace Microsoft Dynamics 365 for Retail (HQ) a kanál lze částečně aktualizovat napříč komponentami. Proto je důležité pochopit, částečné aktualizace ovlivňují funkčnost kupónu jako celek.

- **HQ se aktualizuje částečně, ale nejsou aktualizovány databáze serveru Retail a POS.** V aktualizaci HQ se aktualizují stránky kupónu a slev a modul maloobchodní ceny je rovněž aktualizován. Pokud je aktualizována pouze jedna z těchto dvou komponent, některé stránky v modulu Retail nebudou odpovídat datům výpočtu ceny. Při výpočtech slevy tak mohou nastat neočekávané výpočty slevy nebo chyby.
- **HQ se aktualizuje částečně, ale nejsou aktualizovány databáze serveru Retail a POS (N-1).** Vzhledem k tomu, že zároveň nemohou být aktualizovány všechny maloobchody, doporučujeme, abyste provedli aktualizaci HQ před aktualizací maloobchodů. V případě scénáře N-1 nebude nová funkčnosti vztahující se ke kupónům k dispozici v obchodech, které dosud nebyly aktualizovány. Funkce kupónu například zavádí řádky vyloučení. Používáte-li u slevy vyloučené řádky, nebudou použity v maloobchodě, ve kterém je spuštěna dřívější verze.
- **HQ se neaktualizuje, ale jsou aktualizovány databáze serveru Retail a POS (N+1).** Vzhledem k tomu, že aktualizovaný cenový modul na serveru Retail dokáže zpracovávat zastaralé kódy slev během cenové kalkulace, aktualizace by neměla mít žádný funkční dopad na tento scénář.

