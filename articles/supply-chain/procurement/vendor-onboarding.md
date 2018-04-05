---
title: "Nábor dodavatelů"
description: "Toto téma popisuje proces nabírání nových dodavatelů. Vysvětluje akce, které jsou vyžadovány různými rolemi v průběhu tohoto procesu."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendProspectiveVendorRegistrationRequests,SysUserRequestListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 7265e119a8b59399db1fa35373a7b6aba52ba8e0
ms.contentlocale: cs-cz
ms.lasthandoff: 03/26/2018

---

# <a name="onboard-vendors"></a>Nábor dodavatelů
[!include[banner](../includes/banner.md)]
---

Nové dodavatele lze nabrat a registrovat jako dodavatele v aplikaci Microsoft Dynamics 365 for Finance and Operations na základě informací získaných od osoby, která zastupuje dodavatele.

Proces se skládá z následujících kroků, kde různé role provádějí akce v systému.

1. **Správa dat OData** – Import entit – Počáteční požadavek je požadavek na registraci potenciálního dodavatele. Tento požadavek obvykle pocházejí ze zdroje, jako je například odběratelem hostovaný web umožňující anonymní přístup. Dodavatelé se mohou zaregistrovat zadáním základních informací, jako je název dodavatele, odůvodnění, číslo organizace a jméno a e-mailová adresa kontaktní osoby. Požadavky jsou importovány prostřednictvím rozhraní pro správu dat.
2. **Stránka se seznamem požadavků na registraci potenciálního dodavatele** - Na základě informací, které jsou zadané v požadavku na registraci potenciálního dodavatele, se pracovník zásobování rozhodne, zda bude dodavatel nově přijat. Pracovník zásobování zobrazí příchozí požadavek na stránce se seznamem **Požadavky na registraci potenciálního dodavatele** v aplikaci Finance and Operations.
3. **Workflow zřízení uživatele** - pokud pracovník zásobování ověřil informace v příchozím požadavku a rozhodl se pokračovat s procesem náboru, workflow požadavku uživatele zřídí nového uživatele a odešle e-mailovou pozvánku k přijetí kontaktní osoby jako ověřeného uživatele aplikace Microsoft Dynamics 365.
4. **Průvodce registrace potenciálního dodavatele** - kontaktní osoba dodavatele se přihlásí do aplikace Finance and Operations pomocí nového uživatelského účtu. Tato osoba dokončí průvodce registrace potenciálního dodavatele pro poskytnutí informací, jako jsou adresy, obchodní informace, kategorie zásobování a odpovědi na dotazník.
5. **Workflow schválení** - je vytvořen požadavek na dodavatele, který obsahuje informace o registraci. Požadavek na dodavatele je odeslán do workflowu a přesměrován na kontrolu a schválení.
6. **Vytvoření hlavních dat dodavatele a úprava uživatelské role** – když je schválen požadavek na dodavatele, je vytvořen záznam dodavatele. Uživatelský účet kontaktní osoby dodavatele má buď uděleno oprávnění k dodavatelské spolupráci nebo je deaktivován.

Následující tabulka zobrazuje kroky a role, které jsou zahrnuty v procesu.

| Role a proces       | Správa dat OData – Import entit | Stránka se seznamem požadavků na registraci potenciálního dodavatele | Workflow zřízení uživatele | Průvodce registrací dodavatele | Workflow schválení | Vytvoření hlavních dat dodavatele a úprava uživatelské role |
|--------------------------|---|---|---|---|---|---|
| System                   | Žádost o nového dodavatele je importována. | | | | | Po přijetí oslovení dodavatele je vytvořen záznam dodavatele. |
| Pracovník zásobování | | Spusťte proces náboru. | | | Zkontrolujte a přijměte nebo odmítněte oslovení dodavatele. | |
| Správce            | | | Vytvořte uživatele v aplikaci Finance and Operations a Microsoft Azure. | | | |
| Kontaktní osoba dodavatele    | | | Odešlete e-mail kontaktní osobě. | Zaregistruje informace o dodavateli. | | |

Pro rychlou demonstraci náborového procesu dodavatele se podívejte na toto krátké video na YouTube: 
> [!Video https://www.youtube.com/embed/0KUc3AGaTKk]

## <a name="importing-the-prospective-vendor-registration-request"></a>Import požadavků na registraci potenciálního dodavatele

Požadavek na registraci potenciálního dodavatele je entita v aplikaci Finance and Operations. Systém lze nastavit k importu data prostřednictvím této entity. 

Následující tabulka zobrazuje informace, které tato entita obsahuje a které mohou být importovány.

| Pole                        | popis |
|------------------------------|-------------|
| Název dodavatele                  | Název dodavatele |
| Obchodní odůvodnění       | Důvod(y) požadavku na dodavatele. |
| Číslo organizace          | Oficiálně známé registrační číslo. |
| Odvětví obchodu             | Odvětví obchodu, ze kterého je dodavatel. |
| Křestní jméno kontaktní osoby  | Křestní jméno osoby, která bude pozvána k registraci informací o dodavateli. |
| Druhé jméno kontaktní osoby | Druhé jméno osoby, která bude pozvána k registraci informací o dodavateli. |
| Příjmení kontaktní osoby   | Příjmení osoby, která bude pozvána k registraci informací o dodavateli. |
| E-mail kontaktní osoby       | E-mailová adresa, která se použije k vytvoření nového uživatele v aplikaci Finance and Operations a která bude registrována u klientského účtu Azure Active Directory (Azure AD). |
| Datum odeslání               | Datum vytvoření požadavku v externím systému. |
| Právnická osoba                 | Právnická osoba, u které se dodavatel uchází o to, aby se stal jejím dodavatelem. Tato hodnota musí být kód právnické osoby, který byl registrováno v aplikaci Finance and Operations. Pokud není žádná hodnota přijata prostřednictvím procesu importu, použije se hodnota z parametrů modulu Zásobování a zdroje. |
| Typ dodavatele                  | Dodavatel může být buď organizace, nebo osoba. Typ dodavatele určuje, jak je nakonec dodavatel vytvořen. |

Po importu požadavku na registraci potenciálního dodavatele se tento zobrazí na stránce se seznamem **Požadavek na registraci potenciálního dodavatele**. Z této stránky může pracovník zásobování pozvat uživatele. Požadavek uživatele na zřízení uživatele je odeslání do workflowu.

## <a name="submitting-a-prospective-vendor-user-request"></a>Odeslání požadavku na potenciálního dodavatelského uživatele

Účelem požadavku na potenciálního dodavatelského uživatele je zřízení osoby, která odeslal původní požadavek, aby se mohla přihlásit do aplikace Finance and Operations pomocí e-mailového účtu, který je poskytnut v požadavku na registraci potenciálního dodavatele.

Požadavek potenciálního dodavatelského uživatele bude zpracován workflowem požadavku uživatele. Tento workflow komunikuje prostřednictvím spolupráce Azure AD B2B. Vytvoří uživatele v aplikaci Finance and Operations, který má odpovídající nastavení zabezpečení.

Noví uživatelé, kteří jsou nastaveni, mají následující role zabezpečení:

- Externí uživatel systému
- Potenciální dodavatel (externí)

Nový uživatel obdrží e-mail vygenerovaný workflowem požadavku uživatele. Tento e-mail zve uživatele k přihlášení do systému.

Informace o konfiguraci e-mailu a workflow obecně naleznete v popisu workflow požadavku uživatele v tématu [Nastavení a správa dodavatelské spolupráce](set-up-maintain-vendor-collaboration.md).

## <a name="vendor-registration"></a>Registrace dodavatele

Potenciální dodavatelský uživatel, který se přihlásí do aplikace Finance and Operations, uvidí první stránku průvodce registrací dodavatele, kde si může zadat informace o dodavateli.

Průvodce odráží konfiguraci požadavku na dodavatele. Země nebo oblasti, kde dodavatel provozuje své podnikání, určuje , jaké informace jsou požadovány v průvodci a jaké informace jsou povinné.

Další informace o nastavení konfiguraci požadavku na dodavatele naleznete v tématu [Nastavení a správa dodavatelské spolupráce](set-up-maintain-vendor-collaboration.md). Následující tabulka poskytuje přehled stránek v průvodci a účel každé stránky.

| Stránka                       | popis |
|----------------------------|-------------|
| Země/oblast             | Země nebo oblasti určuje konfiguraci požadavku na dodavatele, která se použije na zbývající stránky průvodce. Určuje také hodnoty ve vyhledávání **Stav daně**. |
| Smluvní podmínky       | Tato stránka může být k dispozici, v závislosti na konfiguraci požadavku na dodavatele. Pokud je k dispozici, musí uživatel potvrdit podmínky, aby mohl pokračovat. |
| Informace o dodavateli         | Tato stránka obsahuje jméno dodavatele, které se automaticky zadá z původního požadavku na registraci potenciálního dodavatele. Také obsahuje číslo organizace, telefonní číslo dodavatele, číslo faxu, e-mailovou adresu a adresy dodavatele pro různé účely. |
| Informace o kontaktní osobě | Tato stránka obsahuje jméno kontaktní osoby, které se automaticky zadá z původního požadavku na registraci potenciálního dodavatele. Obsahuje také telefonní číslo kontaktní osoby a e-mailovou adresu a adresy kontaktní osoby pro různé účely. |
| Obchodní informace       | Tato stránka obsahuje DIČ (pro různé země nebo regiony) a počet zaměstnanců. Rovněž udává, zda se jedná o firmu s menšinovými vlastníky. |
| Kategorie zásobování     | Tato stránka obsahuje kategorie zásobování, pro které vyžaduje dodavatel schválení. Uživatel může vybrat kategorie v hierarchii kategorií zásobování. Počet úrovní, které jsou zobrazeny v hierarchii, lze konfigurovat v možnostech **Parametry modulu Zásobování a zdroje** &gt; **Dodavatelská spolupráce**pod položkami **Zásobování a zdroje** &gt; **Nastavení**. |
| Dotazníky             | Průvodce může obsahovat sadu dotazníků pro dodavatele. Dotazníky, které se zobrazí v průvodci, jsou konfigurovány buď na požadavku na dodavatele nebo podle kategorie zásobování. Pokud jsou dotazníky konfigurovány podle kategorie zásobování, kategorie zásobování, pro které dodavatel požaduje schválení, určují dotazníky, které se zobrazí v průvodci. Na stránce **Kategorie zásobování** můžete přidat dotazník pod příslušnou kategorií a nastavit typ aktivity na **Nábor dodavatele**. |

Když potenciální dodavatelský uživatel dokončí průvodce registrací dodavatele, vytvoří se požadavek na dodavatele.

## <a name="manually-or-automatically-submit-a-vendor-request"></a>Ruční nebo automatické odeslání požadavku na dodavatele

Požadavek na dodavatele může být vytvořen jako koncept ručně odeslán do workflowu. Popřípadě lze požadavek na dodavatele automaticky odeslat do workflowu po dokončení průvodce registrací dodavatele. Požadavek lze odeslat ručně, pokud například pracovník zásobování potřebuje vyhodnotit, zda by měl být požadavek odeslán prostřednictvím procesu schválení předtím, než je odeslán do workflow.

- Vyberte **Parametry modulu Zásobování a zdroje** &gt; **Dodavatelská spolupráce** a poté vyberte **Automaticky odeslat registraci potenciálního dodavatele do workflowu** pro konfiguraci požadavku dodavatele, aby byl odeslán automaticky do workflowu po dokončení průvodce registrace dodavatele.

## <a name="vendor-requests"></a>Oslovení dodavatelů

Požadavky na dodavatele jsou k dispozici na stránce **Uživatelské žádosti dodavatelské spolupráce**.

Požadavek na dodavatele obsahuje informace zadané uživatelem potenciálního dodavatele v průvodci registrací dodavatele.

Požadavek vám umožní zkontrolovat informace o dodavateli a rozhodnout, zda by se měl dodavatel stát registrovaným dodavatelem v aplikaci Finance and Operations.

Požadavek na dodavatele má být odeslán do workflowu a měl by být směrován k příslušné kontrolorům a schvalovatelům. Další základní informace o způsobu nastavení workflowů naleznete v části [Workflowy zásobování a zdrojů](procurement-sourcing-workflows.md).

Následující tabulka ukazuje stavy, které mohou mít požadavky na dodavatele.

| Stav                     | popis |
|----------------------------|-------------|
| Koncept                      | Požadavek na dodavatele ještě nebyl odeslán. |
| Žádost byla odeslána.          | Byl odeslán požadavek na dodavatele a první krok ve workflowu se zpracovává. |
| Čeká na kontrolu             | Pokud existuje více kontrolorů v úkolu workflowu, kontrolor může přijmout úkol revize požadavku na dodavatele a poté dokončit kontrolu. Pokud existuje pouze jeden kontrolor, účastník může dokončit kontrolu výběrem možnosti **Dokončeno** v akci workflowu. Nemusí nejdříve potvrdit položku práce. |
| Žádost čeká na schválení   | Požadavek na dodavatele byl směrován na účastníky pro schválení a je k dispozici možnost požadovat další informace. Žádost o další informace způsobí přesměrování pracovní položky zpět k odesílateli. Požadavek na dodavatele může také být schválen nebo zamítnut, pokud je v tomto stavu. |
| Požadavek na změnu žádosti | Schvalovatel si vyžádal další informace a požadavek na dodavatele byl přesměrován k osobě, která odeslal požadavek na dodavatele. Odesílatel může přidat požadované informace a potom znovu požadavek na dodavatele odeslat. Pokud je požadavek na dodavatele znovu odeslán, stav se změní zpět na hodnotu **Žádost čeká na schválení**. |
| Požadavek schválen           | Tento stav je konečný stav. |
| Žádost byla zamítnuta           | Tento stav je konečný stav. |

## <a name="approving-a-vendor-request"></a>Schválení požadavku dodavatele

Když je požadavek na dodavatele schválen, je vytvořen účet dodavatele a stav **Schváleno** se objeví na počátečním požadavku na registraci potenciálního dodavatele i na požadavku na dodavatele.

Před schválením požadavku na dodavatele na stránce **Nový dodavatel**, na pevné záložce **Obecné** vyberte **Skupina dodavatelů** a vyberte skupinu dodavatelů.

Pokud má mít potenciální dodavatelský uživatel přístup k aplikaci Finance and Operations jako uživatel dodavatelské spolupráce představující dodavatele, nastavte oprávnění k přístupu dodavatelské spolupráce na **Ano**. Chcete-li deaktivovat uživatelský účet, který potenciální dodavatele použil k registraci, nastavte toto oprávnění na **Ne**.

Je-li oprávnění pro přístup k dodavatelské spolupráci nastaven na **Ano**, je po schválení požadavku na dodavatele odeslána žádost na úpravu role uživatele, aby měl uživatel role, které jsou definovány pro typ **Dodavatel** v položce **Externí role**. Je-li toto oprávnění nastaveno na **Ne**, je po schválení požadavku na dodavatele odeslána žádost na deaktivaci uživatele. V takovém případě musí být nastaveno workflow k deaktivaci požadavku uživatele.

Pro účet dodavatele, který má být vytvořen při schválení požadavku na dodavatele, číselná řada pro vytváření dodavatelů z požadavků na dodavatele musí být nastavena na **Automaticky**.

Přehled přístupových oprávnění uživatele dodavatelské spolupráce naleznete v části [Nastavení a správa dodavatelské spolupráce](set-up-maintain-vendor-collaboration.md).

## <a name="rejecting-a-vendor-request"></a>Odmítnutí požadavku na dodavatele

Pokud je požadavek na dodavatele zamítnut, je nutné vybrat důvod pro odmítnutí v požadavku na dodavatele.

Pokud je požadavek na dodavatele zamítnut, je odeslán požadavek na deaktivaci uživatele. V takovém případě musí být nastaveno workflow k deaktivaci požadavku uživatele. Další informace o naleznete v tématu [Nastavení a správa dodavatelské spolupráce](set-up-maintain-vendor-collaboration.md).

Když je požadavek na dodavatele odmítnut, stav **Odmítnuto** se objeví na počátečním požadavku na registraci potenciálního dodavatele i na požadavku na dodavatele.

## <a name="deleting-a-prospective-vendor-registration-request-in-various-statuses"></a>Odstranění požadavku na registraci potenciálního dodavatele v různých stavech

Různé stavy požadavku na registraci potenciálního dodavatele poskytují přehled postupu požadavku.

Pomocí akce **Odstranit** na požadavku registrace potenciálního dodavatele můžete vymazat a odebrat vytvořený řetězec záznamů a deaktivovat uživatelský účet. Výsledek akce **Odstranit** se liší podle stavu požadavku na registraci potenciálního dodavatele, jak je uvedeno v následující tabulce.

| Stav                   | Popis stavu | Výsledek akce odstranění |
|--------------------------|--------------------|-----------------------------------|
| Nová                      | Pro požadavek nebyly provedeny žádné akce. | Požadavek na registraci potenciálního dodavatele je odstraněn. |
| Vyžádáno uživatelem           | Při výběru **Pozvat uživatele** se stav změní na **Vyžádáno uživatelem** a vytvoří se požadavek na potenciálního uživatele, který je odeslán do workflowu požadavku uživatele. | S tímto stavem požadavek na registraci potenciálního dodavatele nelze odstranit, protože nebyl ukončen workflow požadavku uživatele. |
| Pozvaný uživatel             | Workflow pro požadavek uživatele je schválen a uživatel je vytvořen. | Je vytvořen požadavek na deaktivaci uživatele a bude odstraněn požadavek na registraci potenciálního dodavatele. |
| Probíhá registrace | Nový uživatel se přihlásil a spustil průvodce registrace dodavatele. | Je vytvořen požadavek na deaktivaci uživatele a požadavek na registraci potenciálního dodavatele a data, která byla zadána v průvodci registrace dodavatele, budou odstraněna. |
| Požadavek dodavatele vytvořen   | Průvodce registrace dodavatele byl dokončen. | Je vytvořen požadavek na deaktivaci uživatele a požadavek na registraci potenciálního dodavatele a data, která byla zadána v průvodci registrace dodavatele, spolu s požadavkem na dodavatele, budou odstraněna.<blockquote>[!NOTE]<br>Nelze použít akci **Odstranit**, když je požadavek na dodavatele v procesu revize ve workflowu.</blockquote> |
| Schváleno                 | Požadavek na dodavatele je schválen. | Požadavek na registraci potenciálního dodavatele a data, která byla zadána v průvodci registrace dodavatele, spolu s požadavkem na dodavatele, budou odstraněna. |
| Odmítnuto                 | Požadavek na dodavatele je zamítnut. | Požadavek na registraci potenciálního dodavatele a data, která byla zadána v průvodci registrace dodavatele, spolu s požadavkem na dodavatele, budou odstraněna. |

