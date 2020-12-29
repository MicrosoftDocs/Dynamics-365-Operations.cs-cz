---
title: Mobilní pracovní prostor dodavatelské spolupráce
description: Toto téma obsahuje informace o mobilním pracovním prostoru Spolupráce dodavatele Tento pracovní prostor pomáhá udržovat přehled o nákupních objednávkách, které byly odeslány ke schválení dodavatelům. Dále mohou prohlížet informace o nových a aktualizovaných nákupních objednávkách a kontaktech.
author: mkirknel
manager: tfehr
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 267074
ms.assetid: 1d293b3a-2fa2-418d-9347-78c2809d67fe
ms.search.region: global
ms.author: mkirknel
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: fc73fe415ec2b9a266dda6b7f1b3469b7a77f256
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424092"
---
# <a name="vendor-collaboration-mobile-workspace"></a>Mobilní pracovní prostor dodavatelské spolupráce

[!include [banner](../includes/banner.md)]

Toto téma obsahuje informace o mobilním pracovním prostoru **Spolupráce dodavatele**. Tento pracovní prostor pomáhá udržovat přehled o nákupních objednávkách, které byly odeslány ke schválení dodavatelům. Dále mohou prohlížet informace o nových a aktualizovaných nákupních objednávkách a kontaktech.

Tento mobilní pracovní prostor je určen k použití s mobilní aplikací Finance and Operations.

## <a name="overview"></a>Přehled 
Mobilní pracovní prostor **Dodavatelská spolupráce** informuje dodavatele o nových nákupních objednávkách. Dodavatelé si je mohou prohlížet a reagovat na ně pomocí webového klienta pracovní prostor. 

>[!NOTE]
> Mobilní pracovní prostor slouží jako doplněk webového rozhraní dodavatelské spolupráce, nikoli jako jeho náhrada. 

V mobilním pracovním prostoru **Spolupráce dodavatele** si mohou dodavatelé prohlížet nové nákupní objednávky odeslané ke schválení. Zobrazují se zde informace o objednávce, jako jsou produkty, množství a požadovaná data dodání. K dispozici jsou také informace o ceně, v závislosti na konfiguraci jednotlivých dodavatelů. 

Uživatel, který se přihlásí jako dodavatel, uvidí, na které nákupní objednávky již bylo odpovězeno a které stále čekají na akci odběratele. Nákupní objednávka může například čekat na akci zákazníka například v případě, že dodavatel navrhl jiné datum dodání, ale zatím je zatím neschválil. Dodavateli se také zobrazí seznam nákupních objednávek, které jsou potvrzeny, ale nebyly zatím dodány. 

K reakci na nákupní objednávku musí dodavatel použít webové rozhraní pro dodavatelskou spolupráci, které je k dispozici ve webovém klientovi. Tady také dodavatel může o objednávce získat další informace, například přílohy dokumentů, dodací adresy a poplatky spojené s dodavatelem. 

Dodavatelé, kteří mají zvláštní roli zabezpečení, si mohou zobrazovat informace o kontaktních osobách, které jsou u účtů dodavatelů zaregistrovány. Pomocí této role si také může prohlížet stav odeslaných uživatelských žádostí. 

Chcete-li vytvořit nové kontakty a odeslat nové požadavky uživatele, musí být použito webové rozhraní spolupráce dodavatele. 

Mobilní pracovní prostor **Spolupráce dodavatele** umožňuje dodavateli provádět tyto úkoly:

-   zobrazovat nové nákupní objednávky odeslané dodavateli,
-   prohlížet si nákupní objednávky, na které dodavatel zareagoval a které čekají na akci odběratele,
-   zobrazit nákupní objednávky, které jsou potvrzené, ale nebyly ještě plně přijaty,
-   zobrazit informace o kontaktní osobě, která je registrován pro účet dodavatele. (Tato úloha vyžaduje další roli zabezpečení).
-   prohlížet si informace o požadavcích uživatele, které odeslal dodavatel a sledovat jejich stav. (Tato úloha vyžaduje další roli zabezpečení).

## <a name="prerequisites"></a>Předpoklady
Předpoklady se liší podle verze aplikace Microsoft Dynamics 365, která byla nasazena ve vaší organizaci.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Předpoklady při použití aplikace Supply Chain Management
Pokud je ve vaší organizaci nasazena aplikace Supply Chain Management, správce systému musí publikovat mobilní pracovní prostor **Dodavatelská spolupráce**. Více pokynů naleznete v tématu [Publikování mobilního pracovního prostoru](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Předpoklady při použití Microsoft Dynamics 365 for Operations verze 1611 s aktualizací Platform Update 3 nebo vyšší
Pokud je ve vaší organizaci nasazena aplikace Microsoft Dynamics 365 for Operations verze 1611 s aktualizací Platform update 3 nebo novější, správce systému musí dokončit následující předpoklady. 

<table>
<thead>
<tr class="header">
<th>Předpoklad</th>
<th>Role</th>
<th>popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Pokud používáte aktualizace platformy 3, musí být implementován článek KB 3216943.</td>
<td>Správce systému</td>
<td>KB 3216943 je binární aktualizace, která je vyžadována, pokud používáte aktualizaci platformy 3. Pro implementaci tohoto KB musí správce systému provést tyto kroky:
<ol>
<li>Stáhněte si KB 3216943 ze služby Microsoft Dynamics Lifecycle Services (LCS).</li>
<li>Nainstalovat binární aktualizaci, která je dodána jako balíček s možností nasazení. Informace o použití nasaditelného balíčku naleznete v tématu <a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Použití nasaditelného balíčku</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Musí být implementován článek KB 4013633.</td>
<td>Správce systému</td>
<td>KB 4013633 je aktualizace X++ nebo oprava hotfix metadat obsahující mobilní pracovní prostor <strong>Zásoby na skladě</strong>. Pro implementaci KB 4013633 musí správce systému provést tyto kroky:
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Stáhnout opravu hotfix pro metadata z LCS</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Nainstalujte opravu hotfix metadat</a>.</li><li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Vytvořte nasaditelný balíček</a>, který obsahuje model <strong>SCMMobile</strong>, a nahrajte ho do LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Použití nasaditelného balíčku</a></li>
</ol></td>
</tr>
<tr class="odd">
<td>Mobilní pracovní prostor <strong>Spolupráce dodavatele</strong> musí být publikován.</td><td>Správce systému</td>
<td>Viz téma <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publikování mobilního pracovního prostoru</a>.</td>
</tr>
<tr class="even">
<td>Dodavatelský uživatel musí mít přístup k webovému rozhraní dodavatelské spolupráce ve webovém klientovi a musí mít nastaveného uživatele pro dodavatelskou spolupráci.</td><td>Nákupní profesionálové a správce systému</td>
<td>Při nastavování a používání webového rozhraní dodavatelské spolupráce postupujte podle kroků v následujících tématech.
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">Dodavatelská spolupráce s externími dodavateli</a></li>
<li><a href="manage-vendor-collaboration-users.md">Správa uživatelů dodavatelské spolupráce</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">Nastavení a správa dodavatelské spolupráce</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">Práce s odběrateli v aplikaci Supply Chain Management pomocí dodavatelské spolupráce</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Stáhněte a nainstalujte mobilní aplikaci

Stáhněte a nainstalujte mobilní aplikaci Finance and Operations:

-   [Pro telefony Android](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Pro telefony iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Přihlaste se do mobilní aplikace
1.  Spusťte aplikaci na svém mobilním zařízení.
2.  Zadejte URL adresu Microsoft Dynamics 365.
4.  Při prvním přihlášení se zobrazí výzva k zadání uživatelského jména a hesla. Zadejte své přihlašovací údaje.
5.  Po přihlášení se zobrazí dostupné pracovní prostory pro vaši společnost. Všimněte si, že pokud správce systému později publikuje nový pracovní prostor, budete muset aktualizovat seznam mobilních pracovních prostorů.

    [![Vyžádání aktualizace](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="use-the-vendor-collaboration-mobile-workspace"></a>Použití mobilního pracovního prostoru dodavatelské spolupráce
Když vyberete pracovní prostor **Dodavatele spolupráce**, zobrazí se následující možnosti.

![Mobilní pracovní prostor dodavatelské spolupráce](./media/vendor-collaboration-mobile-app.png)

Pracovní prostor **Dodavatele spolupráce** má následující stránky.

### <a name="contacts"></a>Kontakty
Na stránce **Kontakty** si můžete prohlížet všechny kontakty, které byly pro účet dodavatele vytvořeny. Zobrazuje jméno kontaktní osoby, primární e-mailovou adresu a alias uživatele, pokud má kontaktní osoba alias. Tato stránka také uvádí, zda je uživatelský účet kontaktní osoby aktivní. Když vyberete kontakt, zobrazí se kontaktní údaje, jako jsou například právnické osoby, pro které je osoba kontaktem. Můžete také zobrazit kontaktní informace, jako je například telefonní číslo nebo alternativní e-mailová adresa.

### <a name="user-requests"></a>Požadavky uživatele
Na stránce **Požadavky uživatele** se zobrazují všechny uživatelské žádosti odeslané prostřednictvím webového rozhraní dodavatelské spolupráce. Můžete rovněž sledovat stav těchto požadavků. Když vyberete některou uživatelskou žádost, zobrazí se informace o tom, co bylo požadováno, budete moci přidat nebo deaktivovat uživatele, změnit zabezpečení a zjistit, které role zabezpečení byly pro uživatele vyžádány.

### <a name="purchase-orders-ready-for-review"></a>Nákupní objednávky připravené ke kontrole
Na stránce **Nákupní objednávky připravené ke kontrole** se zobrazují všechny nákupní objednávky, které byly odeslány odběratelem a zatím jsou bez reakce. Můžete zobrazit vybrané informace o objednávce, například které produkty byly vyžádány produktech a datu dodání. K dispozici jsou také informace o ceně, v závislosti na konfiguraci dodavatelů.

Zobrazí se i informace o tom, zda nákupní objednávka obsahuje poznámky nebo přílohy. Pokud však chcete otevřít poznámky a přílohy, je nutné použít webové rozhraní spolupráce dodavatele ve webovém klientovi. Výběrem možnosti **Řádek nákupní objednávky** zobrazíte všechny řádky spolu s podrobnostmi. U jednotlivých řádků se zobrazují indikátory poznámek a příloh, nebo informace, zda se dodací adresa liší od adresy uvedené v hlavičce.

Na nákupní objednávky je třeba reagovat pomocí rozhraní dodavatelské spolupráce webového klienta.

### <a name="awaiting-customer-action"></a>Čeká se na akci odběratele.
Na stránce **Čeká se na akci odběratele** najdete nákupní objednávky, na které jste odpověděli vy nebo někdo jiný s přístupem k dodavatelské spolupráci ve vaší společnosti. Nákupní objednávky se v tomto seznamu zobrazují pouze v případě, že má u nich odběratel provést jednu z následujících akcí:

-   Jestliže byla původní nákupní objednávka zamítnuta, odběratel ji musí buď aktualizovat a znovu odeslat, nebo zrušit a znovu odeslat. Po novém odeslání se objednávka přestane zobrazovat na stránce **Čeká se na akci odběratele**.
-   Pokud byla nákupní objednávka přijata se změnami, zákazník musí původní objednávku aktualizovat a znovu odeslat ke kontrole, nebo ji aktualizovat podle požadovaných změn a ihned potvrdit. V obou případech se objednávka na stránce **Čeká se na akci odběratele** už nebude objevovat.
-   Pokud byla nákupní objednávka přijata, ale přesto se zobrazuje se na stránce **Čeká se na akci odběratele**, je to proto, že nebyla při přijetí automaticky potvrzena. V takovém případě čeká na to, až ji nákupčí přidělí stav **Potvrzeno**. Nákupní objednávka se považuje za dohodu mezi odběratelem a dodavatelem, jakmile ji dodavatel přijme. Proto je aktualizace stavu na **Potvrzeno** obvykle pouze formální.

Po výběru nákupní objednávky se zobrazí další podrobnosti o odpovědi. U jednotlivých řádků se zobrazují podrobnosti a odpovědi. Dále je vždy uveden jeden z následujících stavů:

-   Akceptováno
-   Odmítnuto
-   Přijato se změnami
-   Nahrazeno/náhradní
-   Rozdělit na plán / Řádek plánu

Všimněte si, že je hodnota v poli **Dodání** nastavena na **Ano** nebo **Ne** k označení, zda řádky budou dodány. Řádek nemusí být dodán z následujících důvodů:

- Řádek byl odmítnut.
- Náhrada byla provedena a neočekává se, že původní řádek bude doručen podle požadavku v přijatém příkazu.
- Řádek byl rozdělit na více řádků plánu a neočekává se, že původní řádek bude doručen podle požadavku v přijatém příkazu.

Jsou zobrazeny všechny změny, které byly provedeny v odpovědi na řádku objednávky. Odeslané poznámky a přílohy se však nezobrazí. Pokud chcete otevřít poznámky a přílohy, je nutné použít webové rozhraní spolupráce dodavatele ve webovém klientovi.

### <a name="open-confirmed-orders"></a>Otevřít potvrzené objednávky
Jakmile odběratel nákupní objednávku potvrdí (její stav se tedy změní na **Potvrzeno**), objednávka se zobrazí v otevřených potvrzených objednávkách. V seznamu zůstane, dokud ji odběratel nezaregistruje jako přijatou.
