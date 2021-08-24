---
title: Konfigurace pravidel a možností nároků
description: Nastavte pravidla a možnosti nároků ve správě zaměstnaneckých výhod v Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3aae50b8f7fac6991f187ced44f7d122eb7ed40824bd2d53265fa06bfa87dd6a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756117"
---
# <a name="configure-eligibility-rules-and-options"></a>Konfigurace možností a pravidel způsobilosti 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Po nakonfigurování nezbytných parametrů pro správu výhod, můžete vytvářet pravidla způsobilosti, sady, období a programy, které budete přidružovat k plánům zaměstnaneckých výhod.

Pravidla způsobilosti se používají k určení, zda má zaměstnanec nárok na plán. Zaměstnanci musí splňovat podmínku alespoň jednoho pravidla, aby mohli být považováni za způsobilé pro získání výhody. Například máte v plánu dvě pravidla. První pravidlo (řádek 1) uvádí, že typ zaměstnance musí být **Zaměstnanec**. Druhé pravidlo (řádek 2) uvádí, že typ zaměstnance musí být záměstnán na plný úvazek. Zaměstnanci, kteří splňují pravidlo 1, proto mají nárok, i když jsou zaměstnáni pouze na částečný úvazek.

Můžete však nastavit jedno pravidlo, které má více podmínek. V takovém případě zaměstnanci musí splňovat všechny podmínky pravidla, aby mohli být považováni za způsobilé pro získání výhody. Například máte pravidlo s názvem **Zaměstnanec na plný úvazek**. Toto pravidlo uvádí, že typ zaměstnance musí být **Zaměstnanec** *a* zaměstnanec musí být zaměstnán na plný úvazek. Zaměstnanci proto musí splňovat obě podmínky pravidla, aby měli nárok.

> [!IMPORTANT]
> S každým plánem výhod musí být spojeno alespoň jedno pravidlo způsobilosti. K výhodě můžete přidružit více pravidel.

## <a name="create-an-eligibility-rule"></a>Vytvoření pravidla nároku

Pravidla nároku určují, kteří zaměstnanci mohou být přihlášeni v jednotlivých plánech zaměstnaneckých výhod. Po definování pravidel nároku je přiřaďte k plánům zaměstnaneckých výhod. Poté můžete zpracovat nárok na registraci v procesu a zjistit, kteří zaměstnanci mají nárok na jednotlivé plány. 

Během otevřené registrace mohou zaměstnanci vybírat plány zaměstnaneckých výhod. Pokud ztratí nárok na plán zaměstnaneckých na základě pravidel způsobilosti poté, co jsou již registrováni, nebude automaticky zrušena jejich registrace. Obvykle při výskytu životnosti události, která ovlivňuje nárok na plán, je období registrace zahájeno pro zaměstnance k výběru plánů, na které mají nárok. 

1. V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Pravidla a možnosti nároků**.

2. Na kartě **pravidla nároku** vyberte možnost **Nové** a vytvořte pravidlo nároku. Chcete-li zobrazit plány, které jsou přidruženy k pravidlu nároku, vyberte možnost **Připojené plány**.

3. Zadejte hodnoty pro zbývající pole.

   | Pole | popis |
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

4. V části **Další kritéria** vyberte následující možnosti a podle potřeby přidejte informace.

   | Parametr | popis |
   | --- | --- |
   | **Způsobilý věk** | Určuje rozsah nebo rozsahy, které jsou požadovány pro splnění pravidla způsobilosti. |
   | **Způsobilé oddělení** | Určuje oddělení, v němž musí zaměstnanec být, aby splnil pravidlo způsobilosti. |
   | **Způsobilý typ zaměstnání** | Určuje typ nebo typy, v nichž musí zaměstnanec kategorizován, aby splnil pravidlo způsobilosti. Například plný nebo částečný. |
   | **Způsobilá práce** | Určuje úlohu nebo úlohy, které splňují pravidlo způsobilosti. Úlohy jsou spojeny s pozicemi a pozice jsou obsazeny zaměstnanci. |
   | **Způsobilá pracovní funkce** | Určuje pracovní funkci nebo funkce, které splňují pravidlo způsobilosti. Například pracovníci prodeje nebo technici. |
   | **Typ způsobilé práce** | Určuje typ nebo typy úlohy, které splňují pravidlo způsobilosti. Například administrativní nebo vedoucí. |
   | **Způsobilá právnická osoba** | Určuje právnickou osobu nebo právnické osoby, které jsou platné pro pravidlo způsobilosti. Například Contoso Entertainment System USA. |
   | **Způsobilá oblast kompenzace** | Určuje umístění zaměstnance, které splňuje pravidlo způsobilosti. Například zadejte central US. |
   | **Způsobilá pozice** | Určuje pozici nebo pozice, které splňují pravidlo způsobilosti. Například personální asistent nebo manažer HR |
   | **Způsobilý typ pozice** | Určuje typ nebo typy pozice, které splňují pravidlo způsobilosti. Například celý úvazek. |
   | **Způsobilý stav** | Určuje státy nebo provincie, které splňují pravidlo způsobilosti. Například Severní Dakota USA nebo Britská Kolumbie, Kanada. |
   | **Způsobilé podmínky zaměstnání** | Určuje podmínky zaměstnání, které splňují pravidlo způsobilosti. Například podle vůle nebo smlouvy skupiny. |
   | **Způsobilý odbor** | Určuje členství v odborech, která splňují pravidlo způsobilosti. Například řidiči vysokozdvižného vozíku v Americe.</br></br>Použijete-li pravidlo způsobilosti založené na sjednocení, musí se v záznamu sjednocení pracovníka naplnit koncové datum. Nemůžete je nechat prázdné. |
   | **Oprávněné PSČ** | Určuje úlohu nebo úlohy, které splňují pravidlo způsobilosti. Například 58104. |

5. V části **Další podrobnosti** můžete zobrazit následující další podrobnosti.

   | Pole | popis |
   | --- | --- |
   | **Pole způsobilého uživatele** | Určuje další pravidla způsobilosti založená na polích definovaných odběratelem. |
   | **Typ způsobilosti** | Určuje kategorii kritérií, kterou jste vybrali v části **Další kritéria**. |
   | **Odkaz na způsobilost** | Určuje hodnoty, které jste vybrali v části **Další kritéria**. |
   | **Popis** | Popis, který jste vybrali v části **Další kritéria**. |

6. Zvolte možnost **Uložit**.

## <a name="using-custom-fields-in-eligibility-rules"></a>Použití vlastních polí v pravidlech způsobilosti

[Vlastní pole](hr-developer-custom-fields.md) lze vytvořit v rámci Human Resources ke sledování dalších informací. Tato pole lze přidat přímo do uživatelského rozhraní a sloupec se dynamicky přidá do podkladové tabulky.  

V procesu způsobilosti lze použít vlastní pole. Pravidla způsobilosti mohou k určení způsobilosti zaměstnance použít jednu nebo více hodnot vlastních polí.  Chcete-li přidat vlastní pole do existujícího pravidla nebo vytvořit nové pravidlo, přejděte na **Správa zaměstnaneckých výhod > Odkazy > Nastavení > Pravidla způsobilosti > Způsobilost vlastního pole**. Na této stránce můžete vytvořit pravidlo, které používá jedno nebo více vlastních polí, a můžete definovat více hodnot pro každé vlastní pole k určení způsobilosti.

Následující tabulky podporují vlastní pole, která lze použít při zpracování způsobilosti:

- Pracovník (HcmWorker)  
- Úloha (HcmJob)  
- Pozice (HcmPosition)  
- Detail pozice (HcmPositionDetail)  
- Přiřazení pracovníka k pozici  
- Zaměstnání (HcmEmployment)  
- EmploymentDetails (HcmEmploymentDetails)  
- Podrobnosti úlohy (HcmJobDetails)  

Následující typy vlastních polí jsou podporovány při zpracování způsobilosti:

- Text  
- Rozevírací seznam  
- Počet  
- Des. místo  
- Zaškrtávací políčko  

V následující tabulce jsou uvedeny informace o poli vlastního formuláře způsobilosti pole.

| Pole  | popis |
|--------|-------------|
| Jméno | Název vytvářeného kritéria. |
| Název tabulky | Název tabulky obsahující vlastní pole, které se používá pro pravidlo nároků. |
| Název pole | Pole, které bude použito pro pravidlo nároků. |
| Typ operátora | Zobrazí operátor použitý v konfiguraci nároků vlastního pole. |
| Hodnota | Zobrazí hodnotu použitou v konfiguraci nároků vlastního pole. |

## <a name="eligibility-logic"></a>Logika nároků

Následující části popisují, jak jsou zpracovány nároky na zaměstnanecké výhody.

### <a name="rules-assigned-to-a-plan"></a>Pravidla přiřazená k plánu 
Pokud je plánu zaměstnaneckých výhod přiděleno více pravidel nároků, musí zaměstnanec splnit alespoň jedno pravidlo, aby se mohl zaregistrovat do plánu výhod.  V následujícím příkladu musí zaměstnanec splnit požadavky pravidla **Typu práce** nebo pravidla **Aktivní zaměstnanci**.

![Zaměstnanec může splnit požadavky pravidla Typu práce nebo pravidla Aktivní zaměstnanci.](media/RulesAssignedToAPlan.png)
 
### <a name="criteria-within-an-eligibility-rule"></a>Kritéria v rámci pravidla nároků 
V pravidle definujete kritéria, která tvoří pravidlo. Ve výše uvedeném příkladu je kritérium pro pravidlo **Typ práce** místo, kde Typ úlohy = Ředitelé. Zaměstnanec proto musí být ředitelem, aby byl způsobilý. Toto je pravidlo, kde je v pravidle pouze jedno kritérium.

Můžete definovat pravidla, která mají více kritérií. Když definujete více kritérií v rámci pravidla nároků, musí zaměstnanec splnit všechna kritéria v rámci pravidla, aby měl nárok na plán výhod. 

Například výše uvedené pravidlo **Aktivní zaměstnanci** se skládá z následujících kritérií. Aby měl zaměstnanec nárok na základě pravidla **Aktivní zaměstnanci**, musí být zaměstnanec zaměstnán v právnické osobě USMF *a* mít typ pozice na plný úvazek.  

![Kritéria v rámci pravidla nároků.](media/CriteriaWithinAnEligibilityRule.png) 
 
### <a name="multiple-conditions-within-criteria"></a>Více podmínek v rámci kritérií

Pravidla lze dále rozšířit tak, aby používala více podmínek v rámci jednoho kritéria. Zaměstnanec musí splňovat alespoň jednu podmínku, aby měl nárok. Chcete-li navázat na výše uvedený příklad, pravidlo **Aktivní zaměstnanci** lze dále rozšířit o zaměstnance, kteří jsou také zaměstnanci na částečný úvazek. Výsledkem je, že zaměstnanec musí být zaměstnancem v USMF *a* zaměstnanec na plný nebo částečný úvazek.  

![Více podmínek v rámci kritérií.](media/MultipleConditionsWithinCriteria.png) 
 
### <a name="eligibility-conditions-within-a-custom-field-criterion"></a>Podmínky nároků v rámci vlastního kritéria pole 
Podobně jako výše, vlastní pole lze použít při vytváření pravidel nároků a pracovat stejným způsobem. Můžete například nabídnout náhradu za internet zaměstnancům ve Fargu a Kodani, kteří pracují z domova, protože v těchto lokalitách jsou náklady na internet vyšší. Chcete-li to provést, vytvořte dvě vlastní pole: **Umístění kanceláře** (výběr) a **Práce z domova** (zaškrtávací políčko). Poté vytvořte pravidlo s názvem **Zaměstnanci WFH**. Kritériem pravidla je **Umístění kanceláře = Fargo** nebo **Kodaň** *a* **Práce z domova = Ano**.

Je třeba nastavit vlastní pravidla nároků, jak je uvedeno na následujícím obrázku. 

![Podmínky nároků v rámci vlastního kritéria pole.](media/EligibilityConditionsWithinACustomFieldCriterion.png) 
 
## <a name="configure-bundles"></a>Konfigurace svazků

Sady jsou sada souvisejících plánů zaměstnaneckých výhod. Sady zaměstnaneckých výhod lze použít k seskupení plánů zaměstnaneckých výhod, které musí zaměstnanec vybrat, aby bylo možné provést registraci v určitých plánech zaměstnaneckých výhod, které mohou být závislé na registraci plánu zaměstnaneckých výhod. Příklady použití svazku:

- Skupina plánu stavu zahrnující vysoce odpočitatelné zdravotní pojištění s přidruženým účtem zdravotních úspor (HSA).

- Plán životního pojištění s povinným plánem životního pojištění zaměstnance, který je součástí životního plánu závislé osoby. Tím se zaručí, že zaměstnanec nebude moci vybrat životní krytí závislé osoby bez registrace ke krytí zaměstnance.

1. V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Pravidla a možnosti nároků**.

2. Na kartě **Svazky** vyberte možnost **Nový** a vytvořte svazek. Chcete-li zobrazit plány, které jsou přidruženy ke svazku, vyberte možnost **Připojené plány**.

3. Zadejte hodnoty pro zbývající pole.

   | Pole | popis |
   | --- | --- |
   | **Skupina** | Jedinečný identifikátor svazku. |
   | **Popis** | Popis svazku. |
   | **Mistr** | Určuje, zda musí být jeden z plánů ve svazku označen jako hlavní plán. Hlavní plán musí být vybrán během otevřené registrace jako součást svazku, než může správce zaměstnaneckých výhod potvrdit volby zaměstnaneckých výhod. |
   | **Platnost do data a času** | Datum a čas, od kterého je svazek aktivní. |
   | **Platné do** | Datum vypršení platnosti svazku. Výchozí hodnota je 12/31/2154, což znamená nikdy. |

4. Zvolte **Uložit**.

## <a name="configure-periods"></a>Konfigurace období

Období definují, kdy jsou zaměstnanecké výhody v platnosti a kdy se mohou zaměstnanci registrovat. Můžete vytvořit libovolný počet období, aby bylo možné udržovat výhody otevřené registrace a období pokrytí zaměstnaneckých výhod. Roky plánu zaměstnaneckých výhod mohou nebo nemusí následovat po kalendářním roce. 

1. V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Pravidla a možnosti nároků**.

2. Na kartě **Období** vyberte možnost **Nový** a vytvořte období. Chcete-li spustit proces, který připojí všechny platné plány zaměstnaneckých výhod k období zaměstnanecké výhody, **Připojit plány**. Chcete-li zobrazit plány, které jsou přidruženy ke svazku, vyberte možnost **Připojené plány**. 

3. Zadejte hodnoty pro zbývající pole.

   | Pole | popis |
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

3. Vyberte program flexibilního kreditu, který chcete použít. Pole obsahují následující informace.

   | Pole | popis |
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

3. Zadejte hodnoty pro zbývající pole.

   | Pole | popis |
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
