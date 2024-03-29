---
title: Vytvoření plánu zaměstnaneckých výhod
description: V tomto článku je uveden postup při nastavení plánů zaměstnaneckých výhod v aplikaci Dynamics 365 Human Resources.
author: twheeloc
ms.date: 09/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitPlanListPage, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 001318be00efcda1e7ee07513e240059d3c5e135
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643930"
---
# <a name="create-a-benefit-plan"></a>Vytvoření plánu zaměstnaneckých výhod

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

V tomto článku je uveden postup při nastavení plánů zaměstnaneckých výhod v aplikaci Dynamics 365 Human Resources.

1. V pracovním prostoru **Správa zaměstnaneckých výhod** v části **Plány** vyberte možnost **plány zaměstnaneckých výhod**.

2. Zvolte **Nové**.

3. Na kartě **Obecné** zadejte hodnoty pro následující pole:

   | Pole | Popis |
   | --- | --- |
   | **Plán** | Jedinečný identifikátor plánu. |
   | **Popis** | Popis plánu. |
   | **Typ plánu** | Při vytváření nového plánu je nutné zadat typ plánu. Typ plánu je skupina na vysoké úrovni pro specifické typy zaměstnaneckých výhod. Každý typ plánu určuje, zda může zaměstnanec zapsat do více plánů tohoto typu, určuje, zda kontakty jsou příjemci nebo následníci, a definují možnosti disponibility. Můžete vytvořit nové vlastní typy plánů, které budou vyhovovat potřebám nabídek zaměstnaneckých výhod. Hlavní typy plánů zaměstnaneckých výhod: <ul><li>401K</li><li>ADD</li><li>Zubní</li><li>Fitness</li><li>FSA</li><li>Životní</li><li>LTD</li><li>Zdravotní</li><li>PTO</li><li>STD</li><li>Pohled</li></ul> |
   | **Kód typu plánu** | Kód typu plánu. |
   | **Program** | Určuje program, který má volitelně přiřadit plán. |
   | **Sada** | Určuje sadu, která má volitelně přiřadit plán. |
   | **Mistr** | Určuje, zda je plán hlavním plánem v sadě, ke které je přiřazen. |
   | **Požadováno** | Označuje, že je nutné vybrat plán, abyste mohli zkontrolovat jakýkoli jiný plán v sadě. Jako **Požadovaný** může být označen více než jeden plán. V tomto případě všechny plány označené jako **Požadované** bude nutné vybrat, abyste si mohli prohlédnout některý z plánů v sadě.|
   | **Platnost do data a času** | Datum a čas začátku plánu. Výchozí hodnotou je aktuální systémové datum. |
   | **Platný do data a času** | Datum a čas konce plánu. Výchozí hodnota je 12/31/2154, což znamená nikdy.  |

4. Na kartě **Konfigurace** zadejte hodnoty následujících polí v závislosti na typu plánu, který vytváříte:

   | Typ plánu | Pole | Popis |
   | --- | --- | --- |
   | Zdravotnictví (zdravotní, zubní, oční, HMO) | COBRA | Určuje, zda má plán nárok na COBRA (Zákon o sesouhlasení konsolidovaného rozpočtu na Omnibus). |
   | Zdravotnictví (zdravotní, zubní, oční, HMO) | HIPAA | Určuje, zda má plán nárok na HIPAA (zákon o přenositelnost zdravotního pojištění a zodpovědnosti). |
   | Zdravotnictví (zdravotní, zubní, oční, HMO)<br><br>Ostatní (PTO, Fitness)<br><br>Další<br><br>Dlouhodobé postižení<br><br>ADD (základní životní, dobrovolnictví)<br><br>Úspory (například 401 (k))<br><br>FSA | Před zdaněním způsobilý | Určuje, zda lze příspěvky na plán provést před uplatněním daní. |
   | Zdravotnictví (zdravotní, zubní, oční, HMO)<br><br>Ostatní (PTO, Fitness)<br><br>Dlouhodobé postižení<br><br>ADD (základní životní, dobrovolnictví)<br><br>Úspory (například 401 (k))<br><br>FSA | Po zdanění způsobilé | Určuje, zda lze příspěvky na plán provést po uplatnění daní. |
   | Zdravotnictví (zdravotní, zubní, oční, HMO)<br><br>Ostatní (PTO, Fitness)<br><br>Dlouhodobé postižení<br><br>ADD (základní životní, dobrovolnictví)<br><br>Úspory (například 401 (k))<br><br>FSA | Přispěvatel | Určuje, kdo přispívá k plánu – zaměstnanec, zaměstnavatel nebo oba. |
   | Dlouhodobé postižení<br><br>ADD (základní životní, dobrovolnictví) | Minimální pokrytí | Minimální částka pojistného krytí požadovaná pro plán. |
   | Dlouhodobé postižení<br><br>ADD (základní životní, dobrovolnictví) | Maximální pokrytí | Maximální částka pojistného krytí požadovaná pro plán. |
   | Dlouhodobé postižení<br><br>ADD (základní životní, dobrovolnictví) | Použít přírůstky pokrytí | Určuje, zda se má ověřit, zda částka pokrytí odpovídá platné přírůstkové částce. |
   | Dlouhodobé postižení<br><br>ADD (základní životní, dobrovolnictví) | Přírůstková částka | Přírůstková částka pojistného krytí požadovaná pro plán. Je-li například přírůstková částka 1 000, zaměstnanec nemůže mít pojištění ve výši 200 500, kterou by bylo nutné zaokrouhlit nahoru na $201 000 nebo dolů na $200 000. |
   | Dlouhodobé postižení<br><br>ADD (základní životní, dobrovolnictví) | Přírůstkový směr | Určuje směr zaokrouhlení, buď nahoru nebo dolů, když částka pokrytí nesplňuje hodnotu přírůstkové částky. |
   | ADD (základní životní, dobrovolnictví) | Důkaz pojistitelnosti | Určuje, zda zaměstnanec musí poskytovat doklad o pojistitelnosti. |
   | ADD (základní životní, dobrovolnictví) | Množství | Částka v zúčtovací měně. Toto pole je aktivní, jen když je zaškrtnuté políčko Doklad o pojistitelnosti. |
   | Úspory (například 401 (k))<br><br>FSA | Minimální roční příspěvek | Minimální částka příspěvku požadovaná pro plán. |
   | Úspory (například 401 (k))<br><br>FSA | Maximální roční příspěvek | Maximální částka příspěvku požadovaná pro plán. |
   | Úspory (například 401 (k)) | Maximální roční částka zaměstnavatele | Maximální částka, kterou může zaměstnavatel přispívat k plánu úspory zaměstnanců během období zaměstnanecké výhody. Pro použití této možnosti je také nutné zaškrtnout políčko Shoda zaměstnavatele. |
   | Úspory (například 401 (k)) | Dorovnání zaměstnavatele | Určuje, zda zaměstnavatel přispívá k plánu úspor zaměstnance. |
   | Úspory (například 401 (k)) | Procento dorovnání zaměstnavatele | Procento příspěvku zaměstnance, které zaměstnavatel dorovná. |
   | Úspory (například 401 (k)) | Limit dorovnání zaměstnavatele | Maximální procento, které bude zaměstnavatel dorovnávat. Pokud například zaměstnavatel dorovná 100 % příspěvků zaměstnanců až do výše 6 % mzdy zaměstnance, bude se dorovnání zaměstnavatele rovnat 6 %. |

5. Na kartě **Nastavení** zadejte hodnoty pro následující pole:

   | Pole | Popis |
   | --- | --- |
   | **Povolit/pokračovat v zápisu** | Určuje, zda se mohou zaměstnanci registrovat k plánu v případě, že splňují požadavky na způsobilost.</br></br>Pokud je tato možnost nastavena na hodnotu Ne, nebude k dispozici zaměstnancům při zpracování nároku. |
   | **Automatická registrace z předchozího roku** | Určuje, zda automaticky registrovat do plánu způsobilého zaměstnance, pokud byl registrován v předchozím roce. |
   | **Automatická registrace ve výchozím nastavení** | Určuje, zda se má ve výchozím nastavení vybrat plán pro registraci. Plán není povinný, takže zaměstnanec může změnit výchozí výběr. |
   | **Uzavřeno pro nové registrace** | Určuje, zda má být plán omezen pouze na zaměstnance, kteří byli registrováni v plánu v předchozím roce. |
   | **Povinný plán** | Určuje, zda mají být do plánu automaticky registrováni zaměstnanci. Zaměstnanci nemohou měnit výběr registrace. |
   | **Datum počátku** | Datum, kdy byl plán vytvořen ve společnosti. |
   | **Účet dodavatele** (dodavatel zaměstnaneckých výhod) | Dodavatel, kterému společnost zaplatí prémie pro plán. |
   | **Název** (dodavatel zaměstnanecké výhody) | Název dodavatele Toto jméno je vytištěné na dokumentech odesílaných dodavateli, jako jsou např. |
   | **Reference dodavatele** (dodavatel zaměstnaneckých výhod) | Odkaz dodavatele pro plán. Například číslo plánu skupiny společnosti. |
   | **Alternativní reference** (dodavatel zaměstnaneckých výhod) | Alternativní reference dodavatele pro plán. Například číslo účtu společnosti. |
   | **Měna** (dodavatel zaměstnaneckých výhod) | Měna, která se používá k vyplacení pojistného dodavateli. |
   | **Výdajový účet** (dodavatel zaměstnaneckých výhod) | Účet hlavní knihy, který slouží jako výdajový účet pro plánované pojistné. |
   | **Účet dodavatele** (správce zaměstnaneckých výhod) | Dodavatel, kterému společnost zaplatí za správu plánu. Jestliže dochází k samoobslužné správě plánu, ponechte toto pole prázdné. |
   | **Název** (správce zaměstnaneckých výhod) | Název dodavatele správce zaměstnanecké výhody. |
   | **Reference dodavatele** (správce zaměstnaneckých výhod) | Reference dodavatele správce pro plán. |
   | **Alternativní reference** (správce zaměstnaneckých výhod) | Alternativní reference dodavatele správce pro plán. |
   | **Měna** (správce zaměstnaneckých výhod) | Měna, která se používá k vyplacení správci zaměstnaneckých výhod. |
   | **Účet výdajů** (správce zaměstnaneckých výhod) | Účet hlavní knihy, který slouží jako výdajový účet pro náklady spojené se správou plánu. |

6. Na kartě **filtry** podle potřeby proveďte filtrování. Můžete filtrovat podle následujících polí:

   - **Obchodní jednotka**
   - **Oddělení**
   - **Právnická osoba**
   - **Umístění**
   - **Pozice**

7. Na kartě **Pravidla nároku** zadejte hodnoty pro následující pole:

   | Pole | Popis |
   | --- | --- |
   | **Číslo řádku** | Číslo řádku smlouvy pravidla způsobilosti. |
   | **Pravidlo způsobilosti** | Pravidlo způsobilosti, které má být použito pro plán zaměstnaneckých výhod. Toto pravidlo způsobilosti bude použito na odpovídající typ akce a přidruženo k zadanému období čekání na disponibilitu a odpočty. |
   | **Typ akce** | Akce pro uplatnění pravidla způsobilosti pro: vypršení platnosti nebo nároků na zaměstnanecké výhody. |
   | **Čekací doby pokrytí** | Hodnota z formuláře čekajících období. Období čekání na pokrytí určuje počet dní nebo měsíců, kdy zaměstnanec čeká na pokrytí zaměstnanecké výhody nebo vypršení zaměstnanecké výhody na základě kritérií v pravidlu a typu akce. |
   | **Čekací období srážek** | Hodnota z formuláře čekajících období. Období čekání na srážku určuje počet dní nebo měsíců, kdy zaměstnanec čeká na srážku zaměstnanecké výhody z výplaty na základě kritérií v pravidlu a typu akce. |

8. Zvolte **Uložit**.

## <a name="view-enrolled-workers"></a>Zobrazit registrované pracovníky

Můžete zobrazit pracovníky, kteří jsou registrovaní ve vybraném plánu výhod.

1. V pracovním prostoru **Správa zaměstnaneckých výhod** v části **Plány** vyberte možnost **plány zaměstnaneckých výhod**.

2. Na kartě **Výhody** v navigačním panelu vyberte možnost **Zapsaní pracovníci**.

## <a name="attach-coverage-options"></a>Připojit možnosti pokrytí

K vybraným plánům zaměstnaneckých výhod lze přidávat možnosti disponibility. Při připojení možností pokrytí se pro možnost disponibility převede nastavení sazeb a srážek.  Příklad: pro lékařský plán by uživatel mohl vybrat možnost rodinného pokrytí.  Poté by bylo nutné vybrat sazbu rodiny pro přidružený plán (nastavenou v nastavení sazby) a odpočet pro přidružený plán (nastavená v nastavení sazby). To poskytuje náklady pro zaměstnavatele a zaměstnance pro vybrané pokrytí. Poté tento postup zopakujete pro pokrytí zaměstnance+ 1 nebo pokrytí zaměstnance.

1. V pracovním prostoru **Správa zaměstnaneckých výhod** v části **Plány** vyberte možnost **plány zaměstnaneckých výhod**.

2. Na kartě **Výhody** v navigačním panelu vyberte možnost **Připojit možnosti pokrytí**.

## <a name="override-eligibility-rules"></a>Přepis pravidel nároku

Do plánu můžete přidat pracovníky jako výjimky z pravidel způsobilosti. Každý pracovník, kterého přidáte, bude mít nárok na plán zaměstnaneckých výhod.

1. V pracovním prostoru **Správa zaměstnaneckých výhod** v části **Plány** vyberte možnost **plány zaměstnaneckých výhod**.

2. Na kartě **Výhody** v navigačním panelu vyberte možnost **Přepis pravidel nároku**.

## <a name="view-attached-periods"></a>Zobrazit připojená období

Můžete zobrazit seznam dostupných období zaměstnaneckých výhod.

1. V pracovním prostoru **Správa zaměstnaneckých výhod** v části **Plány** vyberte možnost **plány zaměstnaneckých výhod**.

2. Na navigačním panelu vyberte kartu **Období**.

## <a name="view-plan-description"></a>Zobrazení popisu plánu

Můžete zadat popis plánu, který pomůže zaměstnancům s jejich zaměstnaneckými výhodami. Popis plánu, který zde zadáte, se zobrazí v poli Samoobsluha zaměstnance při umístění ukazatele myši na plán v seznamu možnosti pokrytí.

1. V pracovním prostoru **Správa zaměstnaneckých výhod** v části **Plány** vyberte možnost **plány zaměstnaneckých výhod**.

2. Na kartě **Výhody** v navigačním panelu vyberte možnost **Popis plánu**.

## <a name="view-flex-credit-programs"></a>Zobrazit programy flexibilních kreditů

1. V pracovním prostoru **Správa zaměstnaneckých výhod** v části **Plány** vyberte možnost **plány zaměstnaneckých výhod**.

2. Na kartě **Výhody** v navigačním panelu vyberte možnost **Programy flexibilních kreditů**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
