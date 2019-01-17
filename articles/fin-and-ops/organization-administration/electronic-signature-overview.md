---
title: "Elektronické podpisy"
description: "Tento článek obsahuje přehled informací o elektronických podpisech a o možnostech jejich použití v aplikaci Microsoft Dynamics 365 for Finance and Operations."
author: maertenm
manager: AnnBe
ms.date: 08/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 13611
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 676510ef503d51d914ba762e7ac15e2c4811c6ba
ms.contentlocale: cs-cz
ms.lasthandoff: 12/18/2018

---

# <a name="electronic-signatures"></a>Elektronické podpisy

[!include [banner](../includes/banner.md)]

Tento článek obsahuje přehled informací o elektronických podpisech a o možnostech jejich použití v aplikaci Microsoft Dynamics 365 for Finance and Operations.

## <a name="what-is-an-electronic-signature"></a>Co je elektronický podpis?

Elektronický podpis potvrzuje identitu osoby, která spouští nebo schvaluje určitý proces využívající výpočetní techniku. V některých průmyslových odvětvích má elektronický podpis stejnou právní hodnotu jako ruční podpis.

Elektronické podpisy jsou vyžadovány předpisy v několika průmyslových odvětvích, například ve farmaceutickém, potravinářském, leteckém a zbrojním průmyslu. Jsou rovněž nezbytnou podmínkou souladu s předpisy směrnice CFR 21, část 11, kterou vydal Úřad pro kontrolu potravin a léků (FDA) ve Spojených státech amerických.

> [!NOTE]
> Elektronický podpis sám o sobě není totéž jako podpis digitální. Elektronický podpis je prostou náhražkou podpisu psaného rukou, zatímco digitální podpis je doplněn o další bezpečnostní opatření. Digitální podpis vám může pomoci zjistit, zda s daty neoprávněně nemanipuloval jiný uživatel nebo proces. Digitální podpis lze rovněž ověřit, přičemž vlastník certifikátu použitého k podepsání dat nemůže platnost ověření popřít. Jak je popsáno dále, v aplikaci Microsoft Dynamics 365 for Finance and Operations jsou součástí elektronických podpisů i vestavěné funkce podpisů digitálních.

## <a name="electronic-signatures-in-dynamics-365-for-finance-and-operations"></a>Elektronické podpisy v aplikaci Microsoft Dynamics 365 for Finance and Operations

V aplikaci Finance and Operations můžete používat elektronické podpisy pro důležité obchodní procesy. Některé procesy obsahují vestavěné prvky pro práci s elektronickými podpisy. Kromě toho můžete vytvářet vlastní požadavky na podpisy, připojené k libovolné databázové tabulce a poli.

Součástí digitálního podpisu jsou i elektronické podpisy. Každý uživatel, který podepisuje dokumenty, musí získat platný šifrovací certifikát. Při podepsání dokumentu proběhne ověření soukromého klíče přidruženého k použitému certifikátu. Aplikace Finance and Operations ukládá údaje o elektronických podpisech do protokolu, který může sloužit jako záznam auditu. Popis nastavení elektronických podpisů viz [Nastavení elektronických podpisů (Průvodce záznamem úloh)](tasks/set-up-electronic-signatures.md).

## <a name="users-who-require-access-to-electronic-signatures"></a>Uživatelé, kteří potřebují přístup k elektronickým podpisům

Tři druhy uživatelů obvykle vyžadují zabezpečení přístupu k elektronickým podpisům: správci elektronického podpisu, podepisující osoby a auditoři elektronických podpisů.

### <a name="electronic-signature-administrator"></a>Administrátoři elektronických podpisů

Administrátor elektronických podpisů určuje požadavky na podpisy, nastavuje obecné parametry a schvalovatele a přijímá výstrahy v případě, že podpisy nelze ověřit. Ve výchozím nastavení uživatel, který patří do role zabezpečení **Manažer informačních technologií**, má oprávnění ke správě elektronických podpisů.

### <a name="signer"></a>Podepisující uživatel

Podepisující uživatel připojuje elektronické podpisy k dokumentům a procesům, které vyžadují podepsání. Ve výchozím nastavení uživatel, který patří do role zabezpečení **Uživatel systému**, má oprávnění k elektronickému podepisování dokumentů.

> [!NOTE]
> Podepisující uživatel může vyžadovat další oprávnění pro přístup k datům souvisejícím s podepisovaným dokumentem nebo procesem. Uživatel, který mění data a musí provedené změny pak podepsat, musí mít oprávnění ke změnám těchto dat. Uživatel, který podepisuje jménem jiného uživatele nevyžaduje přístup k datům. Příkladem tohoto typu uživatele je nadřízený, který podepisuje změny zaměstnance.

### <a name="electronic-signature-auditor"></a>Auditor elektronických podpisů

Auditor elektronických podpisů kontroluje databázový protokol a kontrolní protokol podpisů, který je k dispozici prostřednictvím databázového protokolu. Ve výchozím nastavení uživatel, který patří do role zabezpečení **Manažer informačních technologií**, má oprávnění k auditu elektronických podpisů.

Pokud má uživatel jinou roli, než **Manažer informačních technologií**, ujistěte se, že jsou roli přiřazena následující oprávnění:

- Zobrazit chyby elektronických podpisů
- Zobrazit protokol databáze

## <a name="signing-documents-electronically"></a>Elektronické podepsání dokumentů

### <a name="get-a-certificate"></a>Získání certifikátu

Před elektronickým podepsáním dokumentů v aplikaci Finance and Operations si musí každý podepisující uživatel vyžádat certifikát.

> [!NOTE]
> Aplikace Finance and Operations používá k vytváření certifikátů a správě elektronického podepisování funkce databázového systému Microsoft SQL Server. Není vyžadována žádná další infrastruktura certifikátů ani veřejných klíčů (PKI).

Vyžádáte-li si certifikát, bude pro vás v databázi aplikace Finance and Operations vytvořen veřejný a soukromý klíč. Soukromý klíč je zašifrován s použitím hesla, které znáte pouze vy. Při elektronickém podepsání dokumentu proběhne ověření vaší totožnosti podle hesla, které zadáte.

Pro zažádání o certifikát klikněte na stránce **Možnosti** na kartě **Účty** na tlačítko **Získat certifikát**.

Zadejte a potvrďte heslo, které budete používat pro podepisování. Heslo slouží k ochraně soukromého klíče a k autorizaci použití vašeho certifikátu. Heslo se neukládá do databáze a nemá k němu přístup nikdo jiný než vy, tj. ani administrátor aplikace Finance and Operations.

Jestliže zapomenete heslo připojené k vašemu certifikátu, musíte tento certifikát vynulovat. Vynulování certifikátu neovlivní dokumenty, které jste podepsali s použitím původního certifikátu. Chcete-li obnovit certifikát, na stránce **Možnosti** klepněte na tlačítko **Obnovit certifikát**.

### <a name="sign-a-document-electronically"></a>Elektronické podepsání dokumentu

Když provedete změnu, která vyžaduje elektronický podpis, zobrazí se stránka **Podepsat dokument**.

1. Na stránce **Podepsat dokument** klepněte na kartu **Dokument** a zkontrolujte provedené změny.
2. Na kartě **Podpis** vyberte kód důvodu.
3. Zadejte komentář, pokud je vyžadován.
4. Není-li v poli **Podepisující uživatel** zobrazeno vaše ID uživatele, vyberte je ze seznamu.
5. Zadejte umístění, pokud jsou tyto informace požadovány.
6. Klepněte na tlačítko **OK**.

### <a name="sign-for-another-users-changes"></a>Podepsat změny jiného uživatele

V určitých situacích je třeba, aby změny provedené jedním uživatelem podepsal jiný uživatel. Příkladem jsou změny kusovníku provedené zaměstnancem, které musí podpisem potvrdit jeho nadřízený. Tento postup použijte, chcete-li určitého uživatele aplikace Finance and Operations ustanovit podepisujícím uživatelem pro jiného uživatele.

> [!NOTE]
> V případě, že jeden uživatel podepisuje změny provedené jiným uživatelem, musí být podpis zadán na pracovní stanici uživatele, který změny provedl. Uživatel nemůže provedené změny uložit, dokud nebudou podepsány.

Chcete-li určit schvalovatele, postupujte takto.

1. Na stránce **Možnosti** na kartě **Účty** klepněte na tlačítko **Určit schvalovatele**.
2. V poli **ID schvalujícího uživatele** vyberte ID uživatele, který musí podepsat změny provedené jiným uživatelem.
3. V poli **Podepsat pro ID uživatele** vyberte ID uživatele, jehož změny musí být podepsány.

