---
title: "Mobilní pracovní prostor dodavatelské spolupráce pro aplikaci Microsoft Dynamics 365 for Operations"
description: "Pomocí mobilního pracovního prostoru dodavatelské spolupráce mohou dodavatelé sledovat aktuální informace o nákupních objednávkách, které jim byly odeslány ke schválení, a prohlížet si údaje o nových a aktualizovaných nákupních objednávkách a kontaktech."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 36 - 37
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267074
ms.assetid: fe8e912d-8446-4584-8a24-d8892e9028cd
ms.search.region: global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 9f441508b745d22218316128572c9ec6aeb7207b
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-collaboration-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Mobilní pracovní prostor dodavatelské spolupráce pro aplikaci Microsoft Dynamics 365 for Operations

Pomocí mobilního pracovního prostoru dodavatelské spolupráce mohou dodavatelé sledovat aktuální informace o nákupních objednávkách, které jim byly odeslány ke schválení, a prohlížet si údaje o nových a aktualizovaných nákupních objednávkách a kontaktech.

<a name="prerequisites"></a>Předpoklady
-------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Předpoklad</th>
<th>popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Přečtěte si o mobilní platformě Microsoft Dynamics 365 for Operations</td>
<td><a href="/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform">Mobilní platforma Microsoft Dynamics 365 for Operations</a></td>
</tr>
<tr class="even">
<td>Dynamics 365 for Operations</td>
<td>Ujistěte se, že používáte prostředí, které má Microsoft Dynamics 365 for Operations verzi 1611 a Microsoft Dynamics for Operations aktualizaci platformy 3 (listopad 2016).</td>
</tr>
<tr class="odd">
<td><span style="color: #000000;">Mobilní zařízení, které má nainstalovanou aplikaci Dynamics 365 for Operations</span></td>
<td><span style="color: #000000;">Stáhněte si aplikaci Dynamics 365 for Operations ze svého obchodu s mobilními aplikacemi.</span></td>
</tr>
<tr class="even">
<td>Oprava KB 3215650</td>
<td>Pomocí této opravy hotfix si zpřístupníte pracovní prostory, které jsou součástí aplikace Dynamics 365 for Operations.</td>
</tr>
<tr class="odd">
<td><span style="color: #ff0000;"><span style="color: #000000;">Oprava KB 3216943</span> </span></td>
<td>Pomocí této opravy hotfix aktivujete mobilní pracovní prostor dodavatelské spolupráce.</td>
</tr>
<tr class="even">
<td>Dodavatelský uživatel musí mít přístup k webovému rozhraní dodavatelské spolupráce v aplikaci 365 Dynamics for Operations a musí mít nastaveného uživatele pro dodavatelskou spolupráci.</td>
<td>Při nastavování a používání webového rozhraní dodavatelské spolupráce postupujte podle pokynů v následujících tématech.
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">Dodavatelská spolupráce s externími dodavateli</a></li>
<li><a href="manage-vendor-collaboration-users.md">Správa uživatelů dodavatelské spolupráce</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">Nastavení a správa dodavatelské spolupráce</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">Práce s odběrateli v aplikaci Dynamics 365 for Operations pomocí dodavatelské spolupráce</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="overview"></a>Přehled
Mobilní pracovní prostor dodavatelské spolupráce informuje dodavatele o nových nákupních objednávkách. Dodavatelé si je mohou prohlížet a reagovat na ně pomocí webového klienta aplikace Dynamics 365 for Operations.  

**Poznámka:** Mobilní pracovní prostor slouží jako doplněk webového rozhraní dodavatelské spolupráce, nikoli jako jeho náhrada.  

V mobilním pracovním prostoru dodavatelské spolupráce si dodavatelé mohou prohlížet nové nákupní objednávky odeslané ke schválení. Zobrazují se zde informace o objednávce, jako jsou produkty, množství a požadované datum dodání. Dostupné informace o ceně závisí na konfiguraci jednotlivých dodavatelů.  

Když se uživatel přihlásí jako dodavatel, uvidí, na které nákupní objednávky již bylo odpovězeno a které stále čekají na akci odběratele. Objednávka může čekat na akci například v případě, že dodavatel navrhl jiné datum dodání, které odběratel zatím neschválil. Dodavateli se také zobrazí seznam nákupních objednávek, které jsou potvrzeny, ale ještě nebyly dodány.  

K reakci na nákupní objednávku musí dodavatel použít webové rozhraní pro dodavatelskou spolupráci, které je k dispozici ve webovém klientovi aplikace Dynamics 365 for Operations. Zde také dodavatel může o objednávce získat další informace, například přílohy dokumentů, dodací adresy a poplatky spojené s dodavatelem.  

V rámci zvláštní role zabezpečení si může dodavatel zobrazovat informace o kontaktních osobách, které jsou u účtů dodavatelů zaregistrovány. Pomocí této role si také může prohlížet stav odeslaných uživatelských žádostí.  

Vytváření nových kontaktů a odesílání nových uživatelských žádostí je třeba provádět v rozhraní pro dodavatelskou spolupráci, které je součástí webového klienta aplikace Dynamics 365 for Operations.  

V mobilním pracovním prostoru může dodavatel provádět toto:

-   zobrazovat nové nákupní objednávky odeslané dodavateli,
-   prohlížet si nákupní objednávky, na které dodavatel zareagoval a které čekají na akci odběratele,
-   zobrazit nákupní objednávky, které mají potvrzený stav, ale nebyly plně přijaty,
-   zobrazovat informace o kontaktních osobách, které jsou zaregistrovány u účtu dodavatel (vyžaduje další roli zabezpečení),
-   prohlížet si informace a sledovat stav uživatelských žádostí odeslaných dodavatelem (vyžaduje další roli zabezpečení).

## <a name="get-started"></a>Začínáme
Chcete-li začít pracovat v mobilním zařízení:

1.  Stáhněte aplikaci Microsoft Dynamics 365 for Operations z obchodu mobilních aplikací.
2.  Spusťte aplikaci na svém zařízení.
3.  Zadejte adresu URL aplikace Dynamics 365.
4.  Zadejte společnost, do které se chcete přihlásit. Například zadejte **USMF**.
5.  Při prvním přihlášení budete vyzváni k zadání uživatelského jména a hesla pro váš účet aplikace Microsoft Dynamics 365 for Operations. 

Po přihlášení do aplikace nejsou zobrazeny žádné pracovní prostory. Pro zobrazení pracovního prostoru ve své mobilní aplikaci musíte nejprve publikovat požadovaný pracovní prostor do aplikace Dynamics 365 for Operations. K publikování pracovního prostoru potřebujete oprávnění správce systému.

1.  Spusťte aplikaci Dynamics 365 for Operations.
2.  Přejděte do nabídky **Správa systému** &gt; **Nastavení** &gt; **systémových parametrů**.
3.  Zvolte **Spravovat aplikaci pro mobilní zařízení**.
4.  K publikování na mobilní platformu vyberte pracovní prostor **Dodavatelská spolupráce**.
5.  Vyberte **Publikovat pracovní prostor**.
6.  Aktualizujte zařízení pro zobrazení publikovaných pracovních prostorů.
7.  Vyberte pracovní prostor **Dodavatelská spolupráce**. Zobrazí se následující stránka.

[![mobilní-aplikace-spolupráce-s-dodavateli](./media/vendor-collaboration-mobile-app.png)](./media/vendor-collaboration-mobile-app.png)

## <a name="contacts"></a>Kontakty
Na stránce **Kontakty** si můžete prohlížet všechny kontakty, které byly pro účet dodavatele vytvořeny. Zobrazují se zde jména kontaktních osob, primární e-mailové adresy a aliasy uživatelů, pokud jsou k dispozici. Také zde zjistíte, zda je uživatelský účet kontaktní osoby aktivní. Po výběru kontaktu se zobrazí podrobnosti o tomto kontaktu (například o tom, které právnické osoby tato osoba zastupuje) a kontaktní informace, jako je telefonní číslo nebo další e-mailová adresa.

## <a name="user-requests"></a>Požadavky uživatele
Na stránce **Požadavky uživatele** se zobrazují všechny uživatelské žádosti odeslané prostřednictvím webového rozhraní dodavatelské spolupráce a jejich stav. Když vyberete některou uživatelskou žádost, zobrazí se informace o tom, co bylo požadováno, budete moci přidat nebo deaktivovat uživatele, změnit zabezpečení a zjistit, které role zabezpečení byly pro uživatele vyžádány.

## <a name="purchase-orders-ready-for-review"></a>Nákupní objednávky připravené ke kontrole
Na stránce **Nákupní objednávky připravené ke kontrole** se zobrazují všechny nákupní objednávky, které byly odeslány odběratelem a zatím jsou bez odpovědi. Můžete zobrazit vybrané informace o objednávce, například o vyžádaných produktech a datu dodání. Informace o ceně jsou dostupné pouze v případě, že je to u dodavatele nakonfigurováno.  

Zobrazí se také informace o tom, zda nákupní objednávka obsahuje poznámky nebo přílohy. K otevření příloh je třeba použít rozhraní dodavatelské spolupráce ve webovém klientovi. Výběrem možnosti **Řádek nákupní objednávky** zobrazíte všechny řádky s podrobnostmi. U jednotlivých řádků se zobrazují indikátory poznámek a příloh, případně toho, že se dodací adresa liší od adresy uvedené v hlavičce.  

Na nákupní objednávky je třeba reagovat pomocí webového klienta dodavatelské spolupráce.

## <a name="awaiting-customer-action"></a>Čeká se na akci odběratele.
Na stránce **Čeká se na akci odběratele** najdete nákupní objednávky, na které jste odpověděli vy nebo někdo jiný s přístupem k dodavatelské spolupráci ve společnosti. Nákupní objednávky se v tomto seznamu zobrazují pouze v případě, že má u nich odběratel provést jednu z následujících akcí.

-   Jestliže byla nákupní objednávka zamítnuta, odběratel ji musí buď aktualizovat a znovu odeslat, nebo zrušit a znovu odeslat. Po novém odeslání objednávka ze stránky **Čeká se na akci odběratele** zmizí.
-   Pokud byla nákupní objednávka přijata se změnami, zákazník musí původní objednávku aktualizovat a znovu odeslat ke kontrole, nebo ji aktualizovat podle změn a ihned potvrdit. V obou případech objednávka ze stránky **Čeká se na akci odběratele** zmizí.
-   Pokud byla nákupní objednávka přijata a zobrazuje se na stránce **Čeká se na akci odběratele**, je to proto, že nebyla při přijetí automaticky potvrzena. V takovém případě čeká na to, až ji nákupčí potvrdí. Nákupní objednávka se obvykle považuje za dohodu mezi odběratelem a dodavatelem, jakmile ji dodavatel přijme. Nastavení potvrzeného stavu nákupní objednávky je pak jen formalitou.

Po výběru nákupní objednávky se zobrazí další podrobnosti o odpovědi. U jednotlivých řádků se zobrazují podrobnosti a odpovědi. Dále je vždy uveden jeden z následujících stavů.

-   Akceptováno
-   Odmítnuto
-   Přijato se změnami
-   Nahrazeno/náhradní
-   Rozdělit na plán / Řádek plánu

Všimněte si indikátoru **Probíhá dodání** = ano/ne, který označuje dodání jednotlivých řádků. Příčinou nedodání může být to, že řádek byl odmítnut nebo nahrazen v případě, že se dodání původních řádků neočekává, nebo to, že byl řádek rozdělen do několika plánů a dodání původního řádku podle přijaté objednávky se neočekává.  

Zobrazují se veškeré změny v odpovědi na řádek objednávky kromě nahraných poznámek a příloh, které si můžete prohlédnout pomocí webového rozhraní dodavatelské spolupráce.

## <a name="open-confirmed-orders"></a>Otevřené potvrzené objednávky
Jakmile odběratel nákupní objednávku potvrdí (její stav se tedy změní na Potvrzeno), objednávka se zobrazí v otevřených potvrzených objednávkách. V seznamu zůstane, dokud ji odběratel nezaregistruje jako přijatou.


