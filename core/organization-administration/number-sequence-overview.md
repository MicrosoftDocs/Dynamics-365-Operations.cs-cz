---
title: "Přehled číselné řady"
description: "Číselné řady v aplikaci Microsoft Dynamics 365 for Operations slouží ke generování srozumitelných jedinečných identifikátorů pro hlavní datové záznamy a záznamy transakcí, které vyžadují identifikátory. Hlavní záznam dat nebo záznam transakce, která vyžaduje identifikátor, je označován jako <em>odkaz</em>."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15461
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: a812c93a13fd36f44e659c9976099af62793098f
ms.lasthandoff: 03/31/2017


---

# <a name="number-sequence-overview"></a>Přehled číselné řady

[!include[banner](../includes/banner.md)]


Číselné řady v aplikaci Microsoft Dynamics 365 for Operations slouží ke generování srozumitelných jedinečných identifikátorů pro hlavní datové záznamy a záznamy transakcí, které vyžadují identifikátory. Hlavní záznam dat nebo záznam transakce, která vyžaduje identifikátor, je označován jako <em>odkaz</em>.

Než bude možné vytvořit nové záznamy pro odkaz v aplikaci Microsoft Dynamics 365 for Operations, je nutné nastavit číselné řady a přidružit je k odkazu. Doporučujeme použít k nastavení číselné řady stránky v modulu **Správa organizace**. Jestliže jsou požadována nastavení modulu, můžete k určení číselných řad pro odkaz v daném modulu použít stránku s parametry v modulu. Například na stránce **Pohledávky** a na stránce **Závazky** můžete nastavit skupiny číselných řad pro přidělení konkrétních číselných řad ke konkrétním odběratelům nebo dodavatelům. Pokud jste nastavili číselnou řadu, musíte zadat obor definující, kterou organizace používá číselná řada. Rozsah může být **Sdílený**, **Společnost**, **Právnická osoba** nebo **Provozní jednotka**. Rozsahy **Právnická osoba** a **Společnost** lze kombinovat s nastavením **Fiskální kalendářní období** a vytvořit tak ještě konkrétnější číselné řady. Formáty číselné řady se skládají ze segmentů. Číselné řady s rozsahem jiným než **Sdílený** mohou obsahovat segmenty, které odpovídají jejich rozsahu. Například číselná řada s rozsahem **Právnická osoba** může obsahovat segment právnické osoby. Zahrnutím rozsahu segmentu ve formátu číselné řady lze identifikovat rozsah určitého záznam zobrazením jeho čísla. Kromě segmentů, které odpovídají rozsahům, mohou formáty číselných řad obsahovat segmenty **Konstanta** a **Alfanumerické**. Segment **Konstanta** obsahuje sadu písmen, číslic a symbolů, které se nemění. Segment **Alfanumerické** obsahuje sadu písmen nebo čísel, které narůstají pokaždé, když se číslo použije. Použijte číselný znak (\#) ke znázornění rostoucích čísel a znak ampersand (&) k označení rostoucích písmen. Formát \#\#\#\#\#\_2017 například vytvoří řadu 00001\_2017, 00002\_2017 atd.
Příklady číselné řady
------------------------

Následující příklady ukazují, jak segmenty slouží k vytváření formátů číselné řady. Konkrétně příklady znázorňují dopad používání segmentů rozsahu.
### <a name="expense-report-numbers"></a>Čísla vyúčtování výdajů

V následujícím příkladu čísla sestavy výdajů jsou přiřazeny k právnické osobě s názvem **CS**. **Oblast: **Cestovné a výdaje **Odkaz: **Číslo vyúčtování výdajů **Rozsah: **Právnická osoba **Právnická osoba: **CS
| Segmenty  | Typ segmentu | Hodnota     |
|-----------|--------------|-----------|
| Segment 1 | Právnická osoba | CS        |
| Segment 2 | Konstanta     | -VýDAJ- |
| Segment 3 | Alfanumerické | \#\#\#\#  |

**Příklad formátovaného čísla**: CS-VÝDAJ-0039 Podobný formát číselné řady můžete nastavit pro další právnické osoby. Například u právnické osoby, která se nazývá **RW**, pokud změníte pouze hodnotu segmentu právnické osoby, formátované číslo bude RW-VÝDAJ-0039. Můžete také změnit celý formát číselné řady pro ostatní právnické osoby. Například můžete vynechat rozsah segmentu právnické osoby k vytvoření formátovaného čísla, jako je Výd-0001.

### <a name="sales-order-numbers"></a>Čísla prodejních objednávek

V následujícím příkladu čísla prodejních objednávek jsou přiřazena k ID společnosti **CEU**. **Oblast: **Prodej**Odkaz: **Prodejní objednávka **Rozsah: **Společnost **Společnost: **CEU
| Segmenty  | Typ segmentu | Hodnota    |
|-----------|--------------|----------|
| Segment 1 | Konstanta     | PO-      |
| Segment 2 | Alfanumerické | \#\#\#\# |

**Příklad formátovaného čísla**: PO-0029 Přestože rozsah segmentu není zahrnut ve formátu, číslování bude restartováno pro každé ID společnosti. Používáte-li pro všechna ID společností stejný formát, stejná čísla se používají v každé společnosti. Například číslo prodejní objednávky SO-0029 je používáno v každé společnosti. Můžete také změnit celý formát číselné řady pro ostatní ID společností.

### <a name="purchase-requisition-numbers"></a>Čísla nákupních žádanek

V následujícím příkladu jsou čísla nákupních žádanek používána pro celou organizaci. **Oblast: **Nákup **Odkaz: **Nákupní žádanka **Rozsah: **Sdílený
| Segmenty  | Typ segmentu | Hodnota    |
|-----------|--------------|----------|
| Segment 1 | Konstanta     | Žád      |
| Segment 2 | Alfanumerické | \#\#\#\# |

**Příklad formátovaného čísla**: Req0052 Vzhledem k tomu, že rozsah je **Sdílený**, formát číselné řady se použije v rámci organizace. Nemůžete nastavit různé formáty číselné řady pro různé části organizace. Předpoklady ohledně výkonu pro číselné řady
-----------------------------------------------

Zvažte následující informace o způsobu konfigurace číselné řady mohou ovlivnit výkonnost systému před nastavením číselných řad.
### <a name="continuous-and-non-continuous-number-sequences"></a>Souvislé a nesouvislé číselné řady

Číselné řady mohou být souvislé nebo nesouvislé. Souvislá číselná řadu nepřeskočí žádná čísla, ale čísla se nesmí používat postupně. Čísla z nesouvislé číselné řady jsou používána postupně, ale sekvence může vynechat čísla. Například pokud uživatel zruší transakcí, číslo se vygeneruje, ale nepoužije. V souvislé číselné řadě se toto číslo použije později. V nesouvislé číselné řadě toto číslo není použito. Souvislé číselné řady jsou obvykle nutné pro externí dokumenty, jako jsou například nákupní objednávky, prodejní objednávky a faktury. Avšak souvislé číselné řady mohou negativně ovlivnit čas odezvy systému vzhledem k tomu, že systém musí požadovat číslo z databáze při každém vytvoření nového dokumentu nebo záznamu. Používáte-li nesouvislou číselnou řadu, můžete povolit možnost **Předběžné přidělení** na pevné záložce **Výkon** na stránce **Číselné řady**. Při zadání množství čísel pro předběžné přidělení vybere systém tato čísla a uloží je do paměti. Nová čísla jsou požadována z databáze, až poté, co bylo použito předběžně přidělené množství. Pokud regulační předpis nepožaduje používání souvislé řady čísel, doporučujeme použít nesouvislé číselné řady pro lepší výkon.

### <a name="automatic-cleanup-of-number-sequences"></a>Automatické vyčištění číselných řad

V případě výpadku napájení, chyby aplikace nebo jiného neočekávaného selhání nemůže systém znovu použít čísla pro souvislé číselné řady. Proces čištění můžete spustit ručně nebo automaticky pro obnovení ztracených čísel. Při plánování procesu čištění pečlivě zvažte použití serveru. Čištění se doporučuje provádět jako dávková úloha mimo pracovní dobu.






