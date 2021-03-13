---
title: Přehled samoobsluhy pro zaměstnance a manažery
description: Tento článek obsahuje přehled o pracovním prostoru samoobsluhy pro zaměstnance a manažery.
author: andreabichsel
manager: tfehr
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f1aadd17b35992af1e79750427fae62e9bd4ff7a
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111758"
---
# <a name="employee-and-manager-self-service-overview"></a>Přehled samoobsluhy pro zaměstnance a manažery

Tento článek obsahuje přehled o pracovním prostoru samoobsluhy pro zaměstnance a manažery.

## <a name="edit-personal-details"></a>Upravit osobní detaily

Chcete-li přidat nebo změnit osobní údaje, viz [Úpravy osobních údajů](hr-employee-manager-self-service-edit-personal-information.md).

## <a name="user-not-assigned-to-a-worker-record"></a>Uživatel není přiřazen k záznamu pracovníka

Pokud jste nepropojili uživatele se záznamem **Pracovník** na stránce **Uživatelé**, zobrazí se následující zpráva:

**Vaše ID uživatele není přidruženo k vašemu záznamu zaměstnance v systému. Před přidružením nebudete moci zobrazit nebo upravit své údaje. Požádejte o asistenci svého manažera nebo tým podpory.**

Chcete-li přidružit uživatele k záznamu **Pracovník**, přejděte na stránku **Uživatelé** a vyberte uživatele. Vyberte možnost **Upravit**, přidejte příslušného pracovníka do pole **Osoba** ve formuláři a vyberte **Uložit**. Nyní byste měli mít přístup k samoobsluze zaměstnanců.

## <a name="security-requirements-for-employee-and-manager-self-service"></a>Bezpečnostní požadavky pro samoobslužnou službu zaměstnanců a manažerů

Samoobslužná služba zaměstnanců a manažerů vyžaduje dvě role zabezpečení:

- Zaměstnanci vyžadují roli Zaměstnanec.
- Manažeři vyžadují roli Zaměstnanec i Manažer.

>[!NOTE]
>Můžete také použít vlastní role pro přístup k samoobslužné službě zaměstnanců a manažerů, pokud jim byl udělen přístup k pracovním prostorům zaměstnanců a manažerů.<br>
>Přístup manažera k informacím o zaměstnancích je založen na hierarchii řádků aktuální pozice v aplikaci Human Resources.

## <a name="employee-self-service"></a>Samoobsluha pro zaměstnance

Na kartě **Moje informace** jsou zobrazeny následující informace pro samoobsluhu zaměstnanců.  

### <a name="summary"></a>Souhrn

Část **Pracovní položky přiřazené mně** zobrazuje všechna schválení a položky workflowu, které jsou přiřazeny zaměstnanci. Položky workflowu můžete konfigurovat, aby uživatelům odesílaly e-maily.

Část **Dotazníky přiřazené mně** zobrazuje všechny plánované dotazníky přiřazené přímo zaměstnanci nebo skupině.

**Adresář společnosti** umožňuje zaměstnancům vyhledat informace související s osobami v organizaci. Veřejné kontaktní informace jsou k dispozici všem zaměstnancům. Adresář společnosti je omezen na společnost, ke které se zaměstnanec přihlásil.

**Týmový kalendář** zobrazuje informace z kalendáře vašeho týmu. Další informace naleznete v tématu [Zobrazení kalendáře týmu a společnosti](hr-employee-self-service-calendar.md).

### <a name="my-career-information"></a>Informace o mé kariéře

Sekce **Moje profesní informace** v samoobsluze pro zaměstnance obsahuje karty související s pracovním volnem a absencí, řízením výkonnosti, kompetencemi, zaměstnaneckými výhodami, úkoly a přílohami.

Na kartě **Zůstatky volna** se zobrazují zůstatky pro všechny registrované plány. Tato karta předpovídá váš zůstatek na základě vaší metody časového rozlišení. Můžete zadat a odeslat požadavky na volno, které pak budou procházet procesem workflowu schválení. Další informace o pracovním volnu a absenci získáte v části [Přehled pracovního volna a absencí](hr-leave-and-absence-overview.md).

Karta **Úkoly** zobrazuje vám přiřazené úkoly a umožňuje jejich prohlížení a správu.

Karta **Příští registrovaný kurz** zobrazuje další kurz, ke kterému jste zaregistrováni. Jakékoli otevřené kurzy můžete zobrazit a registrovat. Všechny kurzy otevřené pro registraci mají stav **Zahájeno** a umožňují zaměstnancům provést samoobslužnou registraci na této kartě. V závislosti na nastavení organizace může registrace kurzu projít schvalovacím procesem.

Karta **Certifikáty** zobrazuje certifikát a datum vypršení platnosti certifikátu nejblíže k aktuálnímu datu. Certifikáty lze aktualizovat, přidávat nebo odebírat. V závislosti na nastavení organizace mohou aktualizace kurzu projít schvalovacím procesem.

Karta **Příští plánované přezkoumání** zobrazuje příští přezkoumání výkonu. Z této karty můžete začít nové přezkoumání. Přezkoumání může iniciovat také vedoucí nebo manažer lidských zdrojů. V závislosti na nastavení organizace můžete také zobrazit, aktualizovat a odesílat výstupní přezkoumání z této karty.

Své cíle můžete spravovat na kartě **Cíle výkonnosti**. Na této kartě je zobrazen počet cílů, které se týkají všech stavů(**Nezahájeno**, **Podle plánu** a **Je třeba zlepšit**). Můžete vytvářet, aktualizovat a odebírat cíle v závislosti na přiřazené roli zabezpečení. Chcete-li, můžete přidat nové cíle ze skupin nebo šablon. Manažeři a oddělení lidských zdrojů mohou rovněž vytvářet cíle místo zaměstnanců a určit, jak podrobné budou jednotlivé cíle. Manažeři a zaměstnanci mohou spolupracovat na cílech a aktualizovat aktivity, měrné systémy a stav. Můžete také zahrnout přílohy.

Své stávající dovednosti si můžete prohlédnout na kartě **Dovednosti**. Můžete aktualizovat dovednosti, přidávat nové nebo odebrat položky, které již nejsou relevantní. V závislosti na nastavení organizace mohou změny dovedností projít schvalovacím procesem.

Aktuální kompenzaci si můžete prohlédnout prostřednictvím karty **Kompenzace**. Výběrem možnosti **Zobrazit** zobrazíte roční částku mzdy a poslední nárůst. Pokud jste zaměstnáni ve více společnostech, každá roční částka se zobrazí na kartě. Chcete-li zobrazit detailní historii kompenzace, vyberte částku ročního platu, čímž a otevřete formulář **Historie fixní a variabilní kompenzace**. Budoucí kompenzace se v tomto formuláři nezobrazuje. Pokud máte více než jedno zaměstnání, můžete přepínat mezi společnostmi v tomto formuláři a zobrazit tak historii kompenzace, aniž byste se museli přihlašovat ke každé společnosti zvlášť.

Dokumenty můžete zobrazit a spravovat na kartě **Přílohy**. Můžete spravovat všechny **Externí** přílohy. Jak oddělení lidských zdrojů, tak i zaměstnanci mohou přidávat přílohy prostřednictvím samoobsluhy pro zaměstnance nebo formuláře **Pracovník**. Ve výchozím nastavení jsou přílohy nastaveny na **Externí**.

### <a name="additional-information"></a>Doplňkové informace

Tato sekce obsahuje odkazy na samoobsluhu pro zaměstnance, podobně jako v sekci **Moje profesní informace**.

K zaměstnaneckým výhodám se můžete registrovat prostřednictvím odkazu **Zaměstnanecké výhody**. Další informace o správě zaměstnaneckých výhod viz [Přehled zaměstnaneckých výhod](hr-benefits-management-overview.md).

V sekci **Výkon** můžete výběrem možnosti **Deníky výkonnosti** vytvořit položky deníku výkonnosti, které se mají používat pro cíle i přezkoumání výkonu. Chcete-li poskytnout zpětnou vazbu ostatním zaměstnancům v rámci organizace, můžete vybrat možnost **Odeslat názor**. V závislosti na nastavení organizace mohou být příjemci, odesilateli a manažerům odesílány e-mailové zprávy. Zpětná vazba může být odeslána všem zaměstnancům v rámci organizace. Odeslání zpětné vazby není omezeno společností.

V části **Kompetence** můžete provádět změny pro **Kurzy**, **Vzdělání**, **Pozice důvěry** a **Profesionální zkušenosti**. V závislosti na nastavení organizace mohou aktualizace těchto kompetencí projít schvalovacím procesem.

Informace o úloze si můžete prohlédnout v části **Organizace**. Podrobnosti o práci zahrnují dovednosti, certifikáty a oblasti odpovědnosti pro primární pozici. Můžete zde také zobrazit vámi vypůjčené vybavení. V závislosti na nastavení organizace mohou změny vypůjčeného vybavení projít schvalovacím procesem.

V části **Dotazník** můžete zobrazit vyplněné dotazníky. Můžete také zobrazit dotazníky v rámci celé společnosti, které nebyly vyplněny. Dotazník můžete kdykoli vyplnit. Autor dotazníku může určit časový rámec a pro který dotazník se použije.

V části **Parametry lidských zdrojů** lze konfigurovat uživatelem definované odkazy. Můžete například definovat odkazy na mzdové výkazy, dokumentaci na konci roku nebo externí softwarová řešení. Tyto odkazy jsou zobrazeny v dolní části této sekce, ale lze je přesunout s použitím individuálního nastavení.

Další karty lze vytvořit také vložením aplikací Power Apps do pracovního prostoru samoobsluhy pro zaměstnance. Pomocí nabídky **Nastavení** můžete stránku přizpůsobit s libovolnou aplikací Power Apps. V nabídce **Nastavení** můžete zvolit přidání aplikace PowerApps, vyplnit podrobnosti a vložit aplikaci. Ve výchozím nastavení se aplikace Power Apps zobrazí jako první karta v pořadí. Pořadí karet lze změnit pomocí standardního přizpůsobení.

## <a name="my-team"></a>Můj tým

Na kartě **Můj tým** jsou zobrazeny následující informace pro samoobsluhu manažerů. Ke kartě **Můj tým** mají přístup pouze manažeři.

### <a name="personnel-actions"></a>Akce personálu

Akce personálu jsou zobrazeny na základě možností konfigurace v částech **Sdílené parametry lidských zdrojů** a **Parametry lidských zdrojů**. Jsou-li povoleny pro **Pracovníky**, mohou akce personálu umožnit nové možnosti nabídky, včetně následujících možností:

- **Požádat o nového zaměstnance**
- **Požádat o nového dodavatele**
- **Požádat o změnu přiřazení pracovníka**
- **Požádat o ukončení poměru**
- **Požádat o změnu kompenzace**

Tyto možnosti lze nakonfigurovat tak, aby procházely volitelným workflowem přezkoumání a schválení.

Povolení možnosti **Akce pozice** povolí následující možnosti:

- **Požádat o novou pozici**
- **Požadavek na změnu podrobností o pozici**

Tyto možnosti lze také nakonfigurovat tak, aby procházely volitelným workflowem přezkoumání a schválení.

### <a name="summary"></a>Souhrn

Informace v části **Souhrn** závisejí na možnostech, které oddělení lidských zdrojů vybralo v části **Parametry lidských zdrojů**. Na kartě **Samoobsluha pro manažery** na stránce **Parametry lidských zdrojů** můžete konfigurovat možnosti pro zobrazení záznamů s končící platností a otevřených pozic. Povolení těchto možností určuje, co se manažerům zobrazí v části **Souhrn**.

Pro manažery můžete konfigurovat následující dlaždice:

- **Certifikáty s končící platností pro můj tým**
- **Identifikační čísla s končící platností pro můj tým**
- **Zkušební doby s končící platností pro můj tým**
- **Prověřování s končící platností pro můj tým**
- **Testy s končící platností pro můj tým**
- **Otevřené pozice pro přímé a/nebo další podřízené**
- **Čekající požadavky na volno pro můj tým**
- **Posouzení dovedností týmu**
- **Analýza dovednostní mezery**
- **Deníky výkonnosti týmu**
- **Cíle výkonnosti týmu**
- **Kontroly výkonnosti týmu**
- **Odcházející pracovníci**

Pro manažery můžete konfigurovat následující možnosti pro provádění změn nebo přidávání žádostí o pracovní volno jménem svých přímých podřízených:

- Certifikáty
- Kurzy
- Položky výpůjčky
- Dovednosti
- Žádosti o pracovní volno a absenci

### <a name="my-team-information"></a>Informace o mém týmu

Informace mého týmu umožňují manažerům zobrazit a aktualizovat přímé a další podřízené. Chcete-li získat přístup k dalším podřízeným, vyberte zaměstnance s přímými podřízenými a poté na kartě vyberte **Zobrazení týmu**. Úplně stejné možnosti se vztahují na další podřízené jako přímé podřízené. 

#### <a name="summary-tab"></a>Karta Souhrn

Karta **Souhrn** poskytuje rychlý přehled o přímých podřízených. Pokud má přímý podřízený také pracovníky, kteří se jim zodpovídají, karta zobrazí počet přímých podřízených v horní části spolu s tlačítkem **Zobrazit tým**. Možnosti nad každou kartou se vztahují k vybranému zaměstnanci. Chcete-li například zadat žádost o volno jménem zaměstnance, vyberte zaměstnance a pak nad kartami zvolte **Požádat o volno**. 

Vyberete-li po výběru zaměstnance tlačítko **Podrobnosti**, zobrazí se následující možnosti:

- **Certifikáty**
- **Kompenzace**
- **Kurzy**
- **Recenze**
- **Pracovní volno**
- **Zapůjčené položky**
- **Cíle výkonnosti**
- **Registrované kurzy**
- **Dovednosti**
- **Odeslat zpětnou vazbu**

V závislosti na nastavení vaší organizace můžete buď provést změny nebo pouze zobrazit.

#### <a name="position-tab"></a>Karta Pozice

Karta **Pozice** obsahuje souhrnné zobrazení zaměstnanců na jejich primární pozici. V oblasti záhlaví každé karty se zobrazí název, dlaždice a oddělení. Tato karta zahrnuje:

- **Datum služebního věku** – zobrazeno z části Souhrn pracovníka ve formuláři pracovníka.
- **Počet let ve společnosti** – výpočet na základě počátečního data zaměstnání zaměstnance.
- **Počet předchozích pozic** – založen na historii pozic; výběrem tohoto počtu otevřete podrobné zobrazení všech dříve zastávaných pozic.
- **Datum narození** – měsíc a den narození zaměstnance.

Můžete zobrazit data pozice pro přímé i další podřízené.

#### <a name="compensation-tab"></a>Karta Kompenzace

Na kartě **Kompenzace** se zobrazuje roční plat zaměstnance. Identifikátor společnosti se zobrazuje pod částkou mzdy. Pokud má zaměstnanec více než jedno zaměstnání a platí jej několik právnických osob, bude mít více plánů kompenzací. Chcete-li zobrazit všechny plány kompenzací napříč právnickými osobami bez změny společnosti, musíte povolit křížovou kompenzaci pod **Lidské zdroje > Sdílené parametry > Pokročilý přístup > Povolit kompenzaci mezi společnostmi**.

Chcete-li zobrazit historii kompenzace, vyberte částku mzdy a otevřete formulář **Podrobnosti**. Ve formuláři **Kompenzace** se zobrazují pouze aktuální a historické záznamy pevných a variabilních kompenzací. Pokud má zaměstnanec více než jedno zaměstnání, můžete přepínat mezi společnostmi a zobrazit historii kompenzací v každé společnosti nebo povolit kompenzaci mezi společnostmi ve sdílených parametrech lidských zdrojů a zobrazit všechny plány kompenzací.

Můžete zobrazit kompenzaci pro přímé i další podřízené.

#### <a name="leave-and-absence-tab"></a>Karta Pracovní volno a absence

Karta **Pracovní volno a absence** zobrazuje nejvyšší zůstatky pro zaměstnance s aktivitou. Chcete-li provést akci nebo zobrazit úplný seznam aktivit, vyberte **Podrobnosti** a pak vyberte možnost **Volno**. Ve formuláři **Volno** můžete zobrazit zůstatky, požadavky, schválené volno a zůstatky prognózy, které zaměstnancům pomáhají lépe spravovat čas. V závislosti na nastavení organizace můžete také požádat o pracovní volno jménem vašich přímých a dalších podřízených.

#### <a name="performance-goals-tab"></a>Karta Cíle výkonnosti

Karta **Cíle výkonnosti** shrnuje cíle výkonnosti podle stavu. Chcete-li zobrazit všechny cíle pro zaměstnance, vyberte číslo pro stav nebo vyberte cíle výkonnosti z části **Podrobnosti**. Manažeři a zaměstnanci mohou podle potřeby aktualizovat cíle v době trvání cíle.

Manažeři mohou zobrazit všechny cíle pro svůj tým prostřednictvím dlaždice **Cíle výkonnosti týmu** v části **Souhrn** na stránce **Můj tým**.

#### <a name="reviews-tab"></a>Karta Přezkoumání

Na kartě **Přezkoumání** je uveden přehled přezkoumání zaměstnance v příslušných stavech: **Probíhá**, **Připraveno k přezkoumání** a **Konečné přezkoumání**. Chcete-li získat přístup k přezkoumání zaměstnance, vyberte tlačítko **Podrobnosti** a pak vyberte přezkoumání, na nichž se chcete podílet. Na základě toho, kde je přezkoumání v rámci procesu workflowu, můžete zjistit, zda je přezkoumání k dispozici pro aktualizaci. 

Všechna přezkoumání pro svůj tým můžete zobrazit prostřednictvím dlaždice **Přezkoumání výkonnosti týmu** v části **Souhrn** pro **Můj tým**.