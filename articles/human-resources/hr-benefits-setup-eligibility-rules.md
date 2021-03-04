---
title: Konfigurace pravidel a možností nároků
description: Nastavte pravidla a možnosti nároků ve správě zaměstnaneckých výhod v Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 70054acafc3aec35fd985c0ca81e928519ddd0a3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417584"
---
# <a name="configure-eligibility-rules-and-options"></a>Konfigurace pravidel a možností nároků

Po nakonfigurování nezbytných parametrů pro správu výhod v Microsoft Dynamics 365 Human Resources můžete vytvářet pravidla způsobilosti, sady, období a programy, které budete přidružovat k plánům zaměstnaneckých výhod.

## <a name="create-an-eligibility-rule"></a>Vytvoření pravidla nároku

Pravidla nároku určují, kteří zaměstnanci mohou být přihlášeni v jednotlivých plánech zaměstnaneckých výhod. Po definování pravidel nároku je přiřaďte k plánům zaměstnaneckých výhod. Poté můžete zpracovat nárok na registraci v procesu a zjistit, kteří zaměstnanci mají nárok na jednotlivé plány. 

Během otevřené registrace mohou zaměstnanci vybírat plány zaměstnaneckých výhod. Pokud ztratí nárok na plán zaměstnaneckých na základě pravidel způsobilosti poté, co jsou již registrováni, nebude automaticky zrušena jejich registrace. Obvykle při výskytu životnosti události, která ovlivňuje nárok na plán, je období registrace zahájeno pro zaměstnance k výběru plánů, na které mají nárok. 

1. V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Pravidla a možnosti nároků**.

2. Na kartě **pravidla nároku** vyberte možnost **Nové** a vytvořte pravidlo nároku. Chcete-li zobrazit plány, které jsou přidruženy k pravidlu nároku, vyberte možnost **Připojené plány**.

3. Zadejte hodnoty pro zbývající pole:

   | Pole | Popis |
   | --- | --- |
   | **Pravidlo způsobilosti** | Jedinečný identifikátor pravidla nároku. |
   | **Popis** | Popis pravidla nároku. |
   | **Platnost do data a času** | Počáteční datum pravidla nároku. | 
   | **Platný do data a času** | Koncové datum pravidla nároku. |
   | **Typ uživatele - zaměstnance** | Určuje, zda má být pro zaměstnance použito pravidlo nároku na zaměstnanecké výhody. |
   | **Typ pracovníka** | Typ pracovníka, pokud je přepínač **Použít typ zaměstnance** nastaven na **Ano**. |
   | **Použít stav zaměstnance** | Určuje, zda má být pro stav zaměstnání zaměstnance použito pravidlo nároku na zaměstnanecké výhody. |
   | **Stav** | Stav zaměstnance, pokud je přepínač **Použít stav zaměstnance** nastaven na **Ano**. Pokud je přepínač **Použít stav zaměstnance** nastaven na **Ne**, toto pole se nepoužívá. |
   | **Použít kategorii zaměstnání** | Určuje, zda má být v rámci pravidla nároku na zaměstnanecké výhody použita hodnota **Kategorie zaměstnání**. | 
   | **Kategorie zaměstnání** | Kategorie zaměstnání zaměstnance v případě, že je přepínač **Použít kategorii zaměstnání** nastaven na **Ano**. |
   | **Použít nové pravidlo náboru** | Určuje, zda má být jako součást pravidla nároku na zaměstnanecké výhody použita nová hodnota období nově přijatého zaměstnance. |
   | **Období registrace** | Časové období, kdy je povolena registrace nově přijatého zaměstnance. Pokud tuto hodnotu nastavíte také v parametrech, nastavení parametrů bude mít přednost před tímto nastavením. |
   | **Použít bývalý stav zaměstnání** | Určuje, zda má být v rámci pravidla nároku na zaměstnanecké výhody použit předchozí stav zaměstnání zaměstnance. Můžete například zadat pravidlo způsobilosti, které odchýlí dobu čekání disponibility pro všechny zaměstnance, kteří přešli ze stavu **Propuštěn** na stav **Zaměstnán** do 90 dnů od jejich předchozího zaměstnání. |

4. V části **Další kritéria** vyberte následující možnosti a podle potřeby přidejte informace:

   | Parametr | Popis |
   | --- | --- |
   | **Způsobilý věk** | Určuje rozsah nebo rozsahy, které jsou požadovány pro splnění pravidla způsobilosti. |
   | **Způsobilé oddělení** | Určuje oddělení, v němž musí zaměstnanec být, aby splnil pravidlo způsobilosti. |
   | **Způsobilý typ zaměstnání** | Určuje typ nebo typy, v nichž musí zaměstnanec kategorizován, aby splnil pravidlo způsobilosti. Například plný nebo částečný. |
   | **Způsobilá práce** | Určuje úlohu nebo úlohy, které splňují pravidlo způsobilosti. Úlohy jsou spojeny s pozicemi a pozice jsou obsazeny zaměstnanci. |
   | **Způsobilá pracovní funkce** | Určuje pracovní funkci nebo funkce, které splňují pravidlo způsobilosti. Například pracovníci prodeje nebo technici. |
   | **Typ způsobilé práce** | Určuje typ nebo typy úlohy, které splňují pravidlo způsobilosti. Například administrativní nebo vedoucí. |
   | **Způsobilá právnická osoba** | Určuje právnickou osobu nebo právnické osoby, které jsou platné pro pravidlo způsobilosti. Například Contoso Entertainment System USA. |
   | **Oblast způsobilá ke kompenzaci** | Určuje umístění zaměstnance, které splňuje pravidlo způsobilosti. Například zadejte central US. |
   | **Způsobilá pozice** | Určuje pozici nebo pozice, které splňují pravidlo způsobilosti. Například personální asistent nebo manažer HR |
   | **Způsobilý typ pozice** | Určuje typ nebo typy pozice, které splňují pravidlo způsobilosti. Například celý úvazek. |
   | **Způsobilý stav** | Určuje státy nebo provincie, které splňují pravidlo způsobilosti. Například Severní Dakota USA nebo Britská Kolumbie, Kanada. |
   | **Způsobilé podmínky zaměstnání** | Určuje podmínky zaměstnání, které splňují pravidlo způsobilosti. Například podle vůle nebo smlouvy skupiny. |
   | **Způsobilý odbor** | Určuje členství v odborech, která splňují pravidlo způsobilosti. Například řidiči vysokozdvižného vozíku v Americe. </br></br>Použijete-li pravidlo způsobilosti založené na sjednocení, musí se v záznamu sjednocení pracovníka naplnit koncové datum. Nemůžete je nechat prázdné. |
   | **Oprávněné PSČ** | Určuje úlohu nebo úlohy, které splňují pravidlo způsobilosti. Například 58104. |

5. V části **Další podrobnosti** můžete zobrazit následující další podrobnosti:

   | Pole | Popis |
   | --- | --- |
   | **Pole způsobilého uživatele** | Určuje další pravidla způsobilosti založená na polích definovaných odběratelem. |
   | **Typ způsobilosti** | Určuje kategorii kritérií, kterou jste vybrali v části **Další kritéria**. |
   | **Odkaz na způsobilost** | Určuje hodnoty, které jste vybrali v části **Další kritéria**. |
   | **Popis** | Popis, který jste vybrali v části **Další kritéria**. |

6. Zvolte **Uložit**.

## <a name="configure-bundles"></a>Konfigurace svazků

Sady jsou sada souvisejících plánů zaměstnaneckých výhod. Sady zaměstnaneckých výhod lze použít k seskupení plánů zaměstnaneckých výhod, které musí zaměstnanec vybrat, aby bylo možné provést registraci v určitých plánech zaměstnaneckých výhod, které mohou být závislé na registraci plánu zaměstnaneckých výhod. Příklady použití svazku:

- Skupina plánu stavu zahrnující vysoce odpočitatelné zdravotní pojištění s přidruženým účtem zdravotních úspor (HSA).

- Plán životního pojištění s povinným plánem životního pojištění zaměstnance, který je součástí životního plánu závislé osoby. Tím se zaručí, že zaměstnanec nebude moci vybrat životní krytí závislé osoby bez registrace ke krytí zaměstnance.

1. V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Pravidla a možnosti nároků**.

2. Na kartě **Svazky** vyberte možnost **Nový** a vytvořte svazek. Chcete-li zobrazit plány, které jsou přidruženy ke svazku, vyberte možnost **Připojené plány**.

3. Zadejte hodnoty pro zbývající pole:

   | Pole | Popis |
   | --- | --- |
   | **Sada** | Jedinečný identifikátor svazku. |
   | **Popis** | Popis svazku. |
   | **Mistr** | Určuje, zda musí být jeden z plánů ve svazku označen jako hlavní plán. Hlavní plán musí být vybrán během otevřené registrace jako součást svazku, než může správce zaměstnaneckých výhod potvrdit volby zaměstnaneckých výhod. |
   | **Platnost do data a času** | Datum a čas, od kterého je svazek aktivní. |
   | **Platné do** | Datum vypršení platnosti svazku. Výchozí hodnota je 12/31/2154, což znamená nikdy. |

4. Zvolte **Uložit**.

## <a name="configure-periods"></a>Konfigurace období

Období definují, kdy jsou zaměstnanecké výhody v platnosti a kdy se mohou zaměstnanci registrovat. Můžete vytvořit libovolný počet období, aby bylo možné udržovat výhody otevřené registrace a období pokrytí zaměstnaneckých výhod. Roky plánu zaměstnaneckých výhod mohou nebo nemusí následovat po kalendářním roce. 

1. V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Pravidla a možnosti nároků**.

2. Na kartě **Období** vyberte možnost **Nový** a vytvořte období. Chcete-li spustit proces, který připojí všechny platné plány zaměstnaneckých výhod k období zaměstnanecké výhody, **Připojit plány**. Chcete-li zobrazit plány, které jsou přidruženy ke svazku, vyberte možnost **Připojené plány**. 

3. Zadejte hodnoty pro zbývající pole:

   | Pole | Popis |
   | --- | --- |
   | **Období** | Jedinečný identifikátor pro období. |
   | **Platnost do data a času** | Počáteční datum a čas, kdy je období zaměstnanecké výhody aktivní. |
   | **Platný do data a času** | Počáteční datum a čas, kdy je období zaměstnanecké výhody neaktivní. |
   | **Začátek registrace** | Počáteční datum pro otevřenou registraci. Otevřená registrace je, když zaměstnanec může v samoobslužných výhodách provádět volby zaměstnaneckých výhod. |
   | **Konec registrace** | Koncové datum pro otevřenou registraci. |
   | **Otevřená** | Určuje, zda je období otevřeno podle systémového data a data a času platnosti od a do. | 
   | **Předchozí období** | Určuje období zaměstnaneckých výhod, které předchází vybranému období zaměstnaneckých výhod. Tyto informace se používají při přihlášení k nárokům na zaměstnanecké výhody k přiřazování plánů, možností disponibility a pověřených osob z předchozího roku. |
 
4. Zvolte **Uložit**.

## <a name="use-a-flex-credit-program"></a>Použití programu flexibilních kreditů

Programy pružného kreditu umožňují registrovat zaměstnance k zaměstnaneckým výhodám podle předem stanoveného počtu pružných kreditů. Zaměstnanci si mohou vybrat způsob přidělení pružných kreditů. Pokud má například zaměstnanec krytí v rámci plánu zdravotního pojištění partnera, může chtít použít kredity, které by se jinak používaly v oblasti zdravotního krytí k jiným dávkám.

1. V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Pravidla a možnosti nároků**.

2. Na kartě **Období** vyberte **Programy flexibilního kreditu**.

3. Vyberte program flexibilního kreditu, který chcete použít. Pole obsahují následující informace:

   | Pole | Popis |
   | --- | --- |
   | ID kreditu zaměstnaneckých výhod | Jedinečný identifikátor programu pro pružné kredity |
   | Popis | Popis programu pro pružné kredity. | 
   | Od data | Datum aktivace programu pružných kreditů. |
   | Do data | Koncové datum programu pružných kreditů. Můžete ponechat výchozí hodnotu (12/31/2154), která označuje, že pružný kredit nemá plánované vypršení platnosti. |
   | Celková hodnota kreditu | Počet kreditů, které bude každý zaměstnanec používat pro své zaměstnanecké výhody. |
   | Pravidlo poměrného rozdělení | Pravidlo, které se použije pro poměrné rozdělení pružných kreditů, když je zaměstnanec zařazen do středu pružného úvěrového období. </br></br><ul><li>**Žádné** – zaměstnanec neobdrží žádné pružné kredity, pokud nastoupí po začátku období programu pružných kreditů.</li><li>**Plný kredit** – zaměstnanec obdrží celou částku pružných kreditů bez ohledu na to, kdy byly přijaty.</li><li>**Poměrně rozložit** – zaměstnanec obdrží průběžnou částku pružných kreditů na základě počátečního data.</li></ul> |
   | Vzorec poměrného rozdělení flexibilního kreditu | Pravidlo, které se použije pro poměrné rozdělení pružných kreditů pro zaměstnance přijaté uprostřed období zaměstnaneckých výhod, když je zaměstnanec zařazen do středu pružného úvěrového období. Poměrné rozložení je založeno na počátečním datu zaměstnání. Toto pole se používá pouze tehdy, pokud vyberete **Poměrně rozložit** v poli **Pravidlo poměrného rozložení**. </br></br><ul><li>**Denně** – poměrně rozloží počet pružných kreditů, které zaměstnanec obdrží na úrovni dní. Celkový počet pružných kreditů je rozdělen podle počtu dní v daném období. Je-li například období zaměstnanecké výhody 400 dní, systém rozdělí celkový počet pružných kreditů na 400 za účelem výpočtu počtu pružných kreditů, které zaměstnanci obdrží za den.</li><li>**Aktuální měsíc** – vyjadřuje počet pružných kreditů, které zaměstnanec obdrží na úrovni měsíce zaokrouhlený na aktuální měsíc. Celkový počet pružných kreditů je rozdělen podle počtu měsíců v daném období. Je-li například období zaměstnanecké výhody 15 měsíců, systém rozdělí celkový počet pružných kreditů na 15 za účelem výpočtu počtu pružných kreditů, které zaměstnanci obdrží za měsíc.</li><li>**Následující měsíc** – vyjadřuje počet pružných kreditů, které zaměstnanec obdrží na úrovni měsíce zaokrouhlený na další měsíc. Celkový počet pružných kreditů je rozdělen podle počtu měsíců v daném období. Je-li například období zaměstnanecké výhody 15 měsíců, systém rozdělí celkový počet pružných kreditů na 15 za účelem výpočtu počtu pružných kreditů, které zaměstnanci obdrží za měsíc.</li></ul> |
   
   Zajistěte, aby byl každý plán zaměstnaneckých výhod registrován pouze jedním příspěvkovým kreditním programem za období zaměstnanecké výhody. V opačném případě systém nebude vědět, který flexibilní kredit se má použít pro poskytnutí flexibilních kreditů a dojde k potížím. 

## <a name="configure-programs"></a>Konfigurovat programy

Programy jsou sadou plánů zaměstnaneckých výhod, které sdílejí společnou sadu pravidel způsobilosti. Pravidla způsobilosti lze definovat pro celý program místo pro každý jednotlivý plán. Jedná se například o program Contoso Canada FTE nebo program na výkonné úrovni Contoso Europe. 

1. V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Pravidla a možnosti nároků**.

2. Na kartě **Programy** vyberte možnost **Nový** a vytvořte program. Chcete-li vytvořit výjimky pro zaměstnance, kteří nesplňují požadavky pravidla způsobilosti, vyberte **Přepis pravidla způsobilosti**. Chcete-li zobrazit plány, které jsou přidruženy k programu, vyberte možnost **Připojené plány**.

3. Zadejte hodnoty pro zbývající pole:

   | Pole | Popis |
   | --- | --- |
   | **Program** | Jedinečný identifikátor pro program. |
   | **Popis** | Popis programu. | 
   | **Platnost do data a času** | Datum a čas, od kterého je program aktivní. |
   | **Platný do data a času** | Datum a čas, kdy vyprší platnost programu. Výchozí hodnota je 12/31/2154, což znamená nikdy. |
   | **Čekací doby pokrytí** | Období, po které musí zaměstnanec čekat, než začne pokrytí pro program zaměstnanecké výhody. |
   | **Čekací období srážek** | Období, po které zaměstnanec čeká, než začne pokrytí pro program zaměstnanecké výhody. |
   | **Pravidla způsobilosti** | Vyberte pravidla způsobilosti, která chcete použít pro program zaměstnaneckých výhod. Pravidla způsobilosti se definují na kartě **Pravidla způsobilosti** na této stránce. |
   
4. Zvolte **Uložit**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]