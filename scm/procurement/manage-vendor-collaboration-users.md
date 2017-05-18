---
title: "Správa uživatelů dodavatelské spolupráce"
description: "Toto téma popisuje, jak můžete požadovat zřízení nových uživatelů dodavatelské spolupráce a přidat nové kontakty dodavatelské spolupráce."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: smmContactPerson, VendVendorContactPerson, VendVendorPortalUser
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 220744
ms.assetid: edc19ad0-3565-4d47-98ac-dda6098f63ac
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 1f1df1e69f3933125bff3eba73d14e8615d7a2a6
ms.contentlocale: cs-cz
ms.lasthandoff: 04/25/2017


---

# <a name="manage-vendor-collaboration-users"></a>Správa uživatelů dodavatelské spolupráce

[!include[banner](../includes/banner.md)]


Toto téma popisuje, jak můžete požadovat zřízení nových uživatelů dodavatelské spolupráce a přidat nové kontakty dodavatelské spolupráce. 

V aplikaci Microsoft Dynamics 365 for Operations jsou k dispozici informace o nákupních objednávkách, fakturách a skladových zásobách pro externí dodavatele. Můžete vytvořit nové kontakty dodavatelské spolupráce a požadovat, aby byli noví uživatelé zajištění, pokud pracujete jako externí dodavatel s rolí zabezpečení **Správce dodavatele (externí)** nebo podobnými oprávněními. Tyto můžete provést také v případě, že pracujete jako odborník na nákup. V tomto tématu odkazuje tato role na odborníky na nákup, kteří pracují pro společnost, která vlastní instanci aplikace Dynamics 365 for Operations. Další informace o použití spolupráce dodavatele, pokud jste externí dodavatel, naleznete v tématu [Dodavatel se zákazníky](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Další informace o použití spolupráce dodavatele, pokud jste odborník na nákup, viz [Spolupráce dodavatele s externími dodavateli](vendor-collaboration-work-external-vendors.md).

## <a name="add-new-vendor-collaboration-contacts"></a>Přidání nových kontaktů dodavatelské spolupráce
Pokud někomu chcete zajistit přístup ke spolupráci dodavatelů, je nutné ho nejdříve přidat jako kontakt spolupráce dodavatelů. Můžete také chtít přidat kontakty pro zaměstnance vaší společnosti, který nepoužívá spolupráci dodavatele. Například to může být kontakt pro jiné druhy informací o nákupu. Nové kontakty se přidávají na stránce **Všechny kontakty** přístupné z nabídky **Dodavatelská spolupráce** &gt; **Kontakty**. Přidání nového kontaktu:

1.  Klepněte na možnost **Nový**.
2.  Zadejte podrobnosti kontaktní osoby.
3.  Vyberte, kterou právnickou osobu představují ve vaší společnosti a se kterou právnickou osobou budou pracovat ve společnosti, se kterou budou spolupracovat. To provedete tak, že vyberete dvojici **Právnická osoba v mé společnosti**/**Právnická osoba ve společnosti odběratele**.
4.  Klepněte na volbu **Vytvořit.**

Pokud chcete odstranit kontakt, je možné odstranit pouze kontakty, které jste vytvořili.

## <a name="vendor-collaboration-user-requests"></a>Uživatelské žádosti dodavatelské spolupráce
Požadavky na uživatele dodavatelské spolupráce může zvýšit profesionál na nákup nebo správce externího dodavatele.

-   Jestliže jste externí dodavatel, můžete odeslat požadavky ze stránky **Všechny kontakty** v rámci modulu **Spolupráce dodavatele**.
-   Pokud jste odborník na nákup, odesíláte požadavky ze stránky **Zobrazit kontakty**. Tento krok lze provést tak, že v záznamu dodavatele v oddílu **Nastavení** podokna akcí vyberete **Kontakty** &gt; **Zobrazit kontakty**.

Lze vytvořit požadavek na zřízení uživatele, na deaktivaci uživatele nebo na změnu rolí zabezpečení Pokud jste správce externího dodavatele, musíte být registrováni jako kontaktní osoba pro účty dodavatele, pro které chcete vytvořit požadavky uživatelů a musíte mít přístup k rozhraní dodavatelské spolupráce pro tyto účty dodavatele.  

Když je odeslán požadavek, je přidán do seznamu **Žádosti uživatelů o dodavatelskou spolupráci** v modulu **Dodavatelská spolupráce** modulu a do seznamu **Požadavek uživatele dodavatelské spolupráce** v modulu **Nákup a zdroje** (Modul Nákup a zdroje není přístupný externím uživatelům).

### <a name="provision-a-user"></a>Zřízení uživatele

Předtím, než můžete požadovat zřízení nového uživatele, musí být tento uživatel nastaven jako kontakt pro jeden nebo více účtů dodavatele. Vytvoření žádosti o nového uživatele dodavatelské spolupráce:

1.  Na stránce **Všechny kontakty** klepněte na **Zřídit dodavatelského uživatele**.
2.  Zadejte e-mailovou adresu uživatele. Uživatel bude tuto adresu používat pro přihlášení do Dynamics 365 for Operations. Pokud e-mailová adresa patří do domény, která je registrována jako tenant v Microsoft Azure, musí být e-mailová adresa existující účte Azure Active Directory (ADD), aby byl proces zřizování úspěšně dokončen. Pokud e-mailová adresa nepatří k doméně registrované službou Microsoft Azure, přidaný účet bude vytvořen jako součást procesu zřizování a nový uživatel obdrží e-mail s pozváním. E-mailové adresy spotřebitelů v doménách jako @hotmail.com, @gmail.com nebo @comcast.net nelze používat k registraci jako uživatele Dynamics 365 for Operations.
3.  Nastavte možnost na **Povolený přístup k dodavatelské spolupráci na** **Ano** pro všechny právnické osoby, ke kterým musí mít uživatel přístup.
4.  V oddílu **Přiřazení rolí uživatelů** zaškrtněte políčko **Přiřadit** pro role zabezpečení, které by měl mít nový uživatel.
5.  Klepněte na tlačítko **Odeslat**.

Při odeslání požadavku dodavatelského uživatele je pole **Povolen přístup dodavatelské spolupráce** nastaveno na hodnotu **Ano** pro vybraný účet dodavatele a je zahájen workflow požadavku uživatele. V rámci tohoto workflowu je v Dynamics 365 for Operations vytvořen nový uživatel a přirazeny role zabezpečení. Kromě toho se aktivuje služba Azure B2B, která iniciuje interakci s portálem Azure a přidruží nový nebo existující účet AAD k uživatelskému účtu Dynamics 365 for Operations.

### <a name="inactivate-a-user"></a>Deaktivace uživatele

Odebrání přístupu uživatele dodavatele spolupráce lze provést dvěma způsoby:

-   Na stránce **Kontakty** pro dodavatele nastavte možnost **Přístup pro dodavatelskou spolupráci je povolen** na **Ne** pro kontakt. To lze provést jednotlivě podle právnických osob, pro které je osoba kontaktem. Tuto možnost mohou používat pouze odborníci na nákup.
-   Deaktivujte celý uživatelský účet odesláním požadavku **Deaktivovat dodavatelského uživatele**.

Vytvoření požadavku na deaktivaci uživatele:

1.  Na stránce **Všechny kontakty** klepněte na **Deaktivovat** **dodavatelského uživatele**.
2.  Do pole **Obchodní odůvodnění** napište komentář.
3.  Klepněte na tlačítko **Odeslat**.

### <a name="modify-security-roles"></a>Změna rolí zabezpečení

Stránka **Spravovat role dodavatelského uživatele** je stejná jako **Zajištění dodavatelského uživatele** s tou výjimkou, že lze upravit seznam rolí zabezpečení.  

Zadání požadavku, aby byly upraveny role zabezpečení pro uživatele:

1.  Na stránce **Všechny kontakty** klepněte na **Spravovat** **role dodavatelského uživatele**.
2.  Do pole **Obchodní odůvodnění** napište komentář.
3.  V části **Spravovat uživatelské role** zaškrtněte políčko u rolí zabezpečení, které chcete přiřadit, nebo zrušte zaškrtnutí políček u rolí, které chcete odstranit.
4.  Klikněte na **Odeslat**.





