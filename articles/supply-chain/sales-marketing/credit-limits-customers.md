---
title: Limity úvěru pro odběratele
description: Tento článek poskytuje přehled o tom, jak fungují úvěrové limity v Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 09/15/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4a98b90491093f55ce6974b9b11ff326c0c2f5c
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015311"
---
# <a name="credit-limits-for-customers"></a>Limity úvěru pro odběratele

[!include [banner](../includes/banner.md)]

Nastavení limitu úvěru vám umožní určit maximální částku úvěru, který poskytnete svým odběratelům. Pokud je limit úvěru určen, je automaticky zkontrolován, když se uživatel pokouší aktualizovat dokument. Při přesažení limitu úvěru se uživateli zobrazí zpráva. Tento článek podává přehled o tom, jak limity úvěrů fungují, a odpovídá na následující dotazy:

-   Jaké dokumenty a procesy mohu zkontrolovat pro limity úvěru?

-   Kde nakonfiguruji způsob, jakým se vypočítá zbývající výše úvěru odběratele?

-   Kde naleznu informace o použitém zbývajícím úvěru odběratele?

-   Kde určím, zda je nutná pro poskytnutí úvěru odběrateli identifikace, a zároveň výši limitu úvěru, která vyžaduje identifikaci?

-   Kde určím, zda zobrazit při překročení limitu úvěru upozornění nebo chybu?

-   Jak určím limit úvěru pro určitého odběratele?

-   Jak ověřím limity úvěru ručně na prodejních objednávkách?

**Jaké dokumenty a procesy mohu zkontrolovat pro limity úvěru?**

Použijte formulář **Parametry pohledávek** pro určení dokumentů, u kterých se zkontrolují limity úvěru. Abyste mohli v tomto formuláři provádět změny, musíte být členem role zabezpečení systému správce (- SYSADMIN –). Limity úvěru můžete zkontrolovat pro následující dokumenty a procesy:

-   Faktury k prodejním objednávkám při zaúčtování faktur

-   Dodací listy pro prodejní objednávky při aktualizaci dodacích listů

-   Prodejní objednávky, když přidáváte řádky do formuláře **Prodejní objednávka**

-   Prodejní objednávky, pokud byly vytvořeny pomocí služby

-   Volné faktury při jejich zaúčtování

Limity úvěru se automaticky zkontrolují, pokud je nastavena jedna ze dvou následujících možností:

-   Ve formuláři **Parametry pohledávek** je nastaveno pole **Typ limitu úvěru** na jakoukoliv možnost jinou než **Žádný**. Limity úvěrů budou kontrolovány pro všechny odběratele.

-   Ve formuláři **Parametry pohledávek** je nastaveno pole **Typ limitu úvěru** na **Žádný**, ale je zvolen **Povinný limit úvěru** pro odběratele ve formuláři **Odběratelé**. Limity úvěrů budou kontrolovány pouze pro konkrétní odběratele.

Abyste mohli zkontrolovat limity úvěru pro následující dokumenty, musíte provést další nastavení.

|    Doklad                                    |    Další nastavení                                                                                                             |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|    Volná faktura                         |    Ve formuláři Parametry pohledávek v oblasti Třída úvěruschopnosti zvolte Kontrola limitu úvěru ve faktuře s volným textem.     |
|    Prodejní objednávka (zadáno ručně)            |    Ve formuláři Parametry pohledávek v oblasti Třída úvěruschopnosti zvolte Kontrola limitu úvěru na prodejní objednávce.           |
|    Prodejní objednávka (elektronicky přijatá)     |    Ve formuláři Parametry pohledávek v oblasti AIF zvolte Zkontrolovat limit úvěru pro prodejní objednávky.                     |

**Kde nakonfiguruji způsob, jakým se vypočítá zbývající výše úvěru odběratele?**

Můžete nakonfigurovat Dynamics 365 tak, aby vypočítal zbývající kredit odběratele jedním z následujících způsobů:

-   Srovnáním limitu úvěru vůči zůstatku odběratele.

-   Srovnáním limitu úvěru vůči zůstatku odběratele a částkám na dodacích listech.

-   Srovnáním limitu úvěru vůči zůstatku odběratele a všem otevřeným aktivitám transakcí. To zahrnuje částky na dodacích listech a částky prodejních objednávek.

Použijte formulář **Parametry pohledávek** k zadání informací, vůči kterým bude probíhat srovnání. Abyste mohli v tomto formuláři provádět změny, musíte být členem role zabezpečení systému správce (- SYSADMIN –). V poli **Typ limitu úvěru** vyberte, zda se mají provést kontroly limitů úvěru a jaké informace o transakci mají být zahrnuty při kontrole limitu úvěru. Vyberte některou z následujících možností:

-   **Žádný** – Nekontrolují se limity úvěrů. Tuto možnost pro určitého odběratele můžete přepsat výběrem zaškrtávacího políčka **Povinný limit úvěru** ve formuláři **Odběratelé**. Pokud tak učiníte, limit úvěru se kontroluje vůči zůstatku odběratele.

-   **Zůstatek** – limit úvěru se kontroluje vůči zůstatku odběratele.

-   **Zůstatek + dodací list nebo příjemka produktu** – limit úvěru se kontroluje vůči zůstatku odběratele a dodávkám.

-   **Zůstatek + vše** – limit úvěru se kontroluje vůči zůstatku odběratele, dodávkám a otevřeným objednávkám.

**Kde naleznu informace o použitém zbývajícím úvěru odběratele?**

Informace o zůstatku odběratele a částce úvěru se vypočítají a uloží při vytvoření snímku sledování splatnosti a zobrazí se ve formuláři **Inkasa**. Částky, které jsou zobrazeny ve formuláři **Inkasa** nemusí zahrnovat všechny aktivity transakce, dokud není vytvořen snímek sledování splatnosti. Další informace naleznete v tématu [Inkasa a úvěr v modulu Pohledávky](/dynamicsax-2012/appuser-itpro/collections-and-credit-in-accounts-receivable).

V závislosti na zvolených dokumentech se vypočítá informace o zůstatku odběratele a zbývající částka úvěru při aktualizaci prodejních objednávek, dodacích listů a faktur odběratele. Pokud by částka dokumentu, se kterým pracujete, způsobila překročení limitu úvěru, zobrazí se zpráva.

**Kde určím, zda je nutná pro poskytnutí úvěru odběrateli identifikace, a zároveň výši limitu úvěru, která vyžaduje identifikaci?**

Použijte formulář **Parametry pohledávek** k určení, zda má být vyžadována identifikace a, určení částky limitu úvěru vyžadující identifikaci.
Abyste mohli v tomto formuláři provádět změny, musíte být členem role zabezpečení systému správce (- SYSADMIN –).

|    Pole                                    |    popis                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    Požadavek identifikace k úvěru     |    Vyberte způsob identifikace, který je nutné zadat pro odběratele, kterým vaše právnická osoba poskytuje úvěr. Možnost, kterou vyberete v tomto poli, určuje, kdy a jaké typy informací jsou vyžadovány v polích Identifikační údaje pro státní správu ve formuláři Odběratelé:         Ne - Nevyžaduje se identifikace vydaná státní správou, bez ohledu na limit úvěru odběratele.     Ano – Vyžaduje se licenční číslo nebo identifikace vydané státní správou, pokud je limit úvěru odběratele větší nebo rovný nule.     Minimální limit – Licenční číslo nebo identifikace vydané státní správou se vyžadují, pokud je limit úvěru odběratele větší nebo roven limitní hodnotě, kterou jste zadali v poli Limit v tomto formuláři.        |
|    Limit                                    |    Zadejte limit úvěru, při kterém je u odběratele vyžadováno licenční číslo nebo jiná identifikace vydaná státní správou.    Pokud například chcete, aby pro odběratele s limitem úvěru 2000 nebo vyšším bylo vyžadováno identifikační číslo (například číslo občanského průkazu), zadejte hodnotu 2000.    Toto pole je k dispozici, pokud vyberete hodnotu Minimální limit v poli Požadovat identifikační údaje při úvěru.                                                                                                                                                                                                                                                                                                                                                                                                                                         |

**Kde určím, zda zobrazit při překročení limitu úvěru upozornění nebo chybu?**

Použijte formulář **Parametry pohledávek** k určení, zda chcete při překročení limitu úvěru zobrazit upozornění nebo chybu. Toto upozornění nebo chyba se zobrazí tehdy, když uživatel zadává nebo zaúčtovává informace, nebo budou zahrnuty do protokolu, pokud jsou dokumenty zpracovány elektronickou službou. Abyste mohli v tomto formuláři provádět změny, musíte být členem role zabezpečení systému správce (- SYSADMIN –).

|    Pole                                                               |    popis                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    Zpráva při překročení limitu úvěru (v oblasti Třída úvěruschopnosti)     |    Zvolte si způsob zobrazení zpráv o překročení limitu úvěru pro uživatele. Vyberte některou z následujících možností:       Chyba – Zobrazí se chybová zpráva. Obvykle se zastaví aktuální informace, a než bude moci proces pokračovat, musí být konflikt vyřešen.     Upozornění – Zobrazí se upozornění, ale proces může pokračovat.                     |
|    Zpráva při překročení limitu úvěru (v oblasti AIF)               |    Zvolte si způsob doručení zpráv o překročení limitu úvěru v protokolu. Vyberte některou z následujících možností:    Chyba – Zobrazí se chybová zpráva ve formuláři Výjimky a dokument se nezpracuje do vyřešení chyby.     Upozornění – Zobrazí se upozornění ve formuláři Výjimky, ale proces může pokračovat.        |

**Jak určím částku limitu úvěru pro určitého odběratele?**

Použijte formulář **Odběratelé** k určení částky limitu úvěru pro určitého odběratele. Musíte být členem role zabezpečení, která má k sobě přiřazené funkční oprávnění Spravovat hlavní data odběratele (CustCustomersMaintain), abyste v tomto formuláři mohli provádět změny.

1.  Klikněte na **Pohledávky** \> **Zákazníci** \> **Všichni zákazníci**. Klikněte dvakrát na účet odběratele.

2.  Ve formuláři **Odběratelé** v podokně akcí klikněte na **Upravit**.

3.  Do pole **Limit úvěru** zadejte částku měny. Tato hodnota musí být větší než nula (0) a použije se jako částka limitu úvěru.

4.  V případě potřeby zadejte licenční číslo nebo jinou identifikaci vydané státní správou do pole **Identifikační údaje pro státní správu**.

> [!NOTE]
> Ve formuláři **Parametry pohledávek** obvykle zvolíte typ limitu úvěru. Pokud je však typ limitu úvěru nastaven na **Žádný**, je nutné vybrat také zaškrtávací políčko **Povinný limit úvěru** ve formuláři **Odběratelé** s cílem zkontrolovat limit úvěru vůči zůstatku odběratele. Další informace týkající se typů limitu úvěru naleznete v části Jaké dokumenty a procesy mohu zkontrolovat pro limity úvěru? v tomto článku. 

**Jak ověřím limity úvěru ručně na prodejních objednávkách?**

V některých případech je třeba ručně zkontrolovat limit úvěru odběratele. Například může ručně zkontrolovat limit úvěru odběratele před zahájením zadávání prodejní objednávky. K ruční kontrole limit úvěru lze použít formulář **Prodejní objednávka**. Musíte být členem role zabezpečení, která má k sobě přiřazené funkční oprávnění Spravovat prodejní objednávku (SalesOrderMaintain), abyste v tomto formuláři mohli provádět změny.

1.  Klikněte na **Prodej a marketing** \> **Prodejní objednávky** \> **Všechny prodejní objednávky**. Dvakrát klikněte na prodejní objednávku.

2.  Ve formuláři **Prodejní objednávka** v podokně akcí na kartě **Spravovat**, klikněte na **Zkontrolovat limit úvěru**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]