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
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 380f1bcdf7109dc12fd898199033eac7710d863c
ms.lasthandoff: 03/31/2017


---

# <a name="manage-vendor-collaboration-users"></a>Správa uživatelů dodavatelské spolupráce

[!include[banner](../includes/banner.md)]


Toto téma popisuje, jak můžete požadovat zřízení nových uživatelů dodavatelské spolupráce a přidat nové kontakty dodavatelské spolupráce. 

V aplikaci Microsoft Dynamics 365 for Operations jsou k dispozici informace o nákupních objednávkách, fakturách a skladových zásobách pro externí dodavatele. Můžete vytvořit nové kontakty dodavatelské spolupráce a požadovat, aby byli noví uživatelé zajištění, pokud pracujete jako externí dodavatel s rolí zabezpečení **Správce dodavatele (externí)** nebo podobnými oprávněními. Tyto můžete provést také v případě, že pracujete jako odborník na nákup. V tomto tématu odkazuje tato role na odborníky na nákup, kteří pracují pro společnost, která vlastní instanci aplikace Dynamics 365 for Operations. Další informace o použití spolupráce dodavatele, pokud jste externího dodavatele naleznete v tématu [dodavatele se zákazníky](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Další informace o použití spolupráce dodavatele, pokud jste profesionální zadávání vládních zakázek naleznete v tématu [spolupráce s externími dodavateli, dodavatel](vendor-collaboration-work-external-vendors.md).

## <a name="add-new-vendor-collaboration-contacts"></a>Přidání nových kontaktů dodavatelské spolupráce
Pokud někomu chcete zajistit přístup ke spolupráci dodavatelů, je nutné ho nejdříve přidat jako kontakt spolupráce dodavatelů. Můžete také chtít přidat kontakty pro zaměstnance vaší společnosti, který nepoužívá spolupráci dodavatele. Například to může být kontakt pro jiné druhy informací o nákupu. Nově přidaných kontaktů na **všechny kontakty** stránky, které je přístupné z **spolupráce dodavatele**&gt;**kontakty** nabídky. Přidání nového kontaktu:

1.  Klepněte na možnost **Nový**.
2.  Zadejte podrobnosti kontaktní osoby.
3.  Vyberte, kterou právnickou osobu představují ve vaší společnosti a se kterou právnickou osobou budou pracovat ve společnosti, se kterou budou spolupracovat. Provedete to vybráním **právnické osoby v mé firmě**/**právnické osoby ve firmě zákazníka** pár.
4.  Klepněte na volbu **Vytvořit.**

Pokud chcete odstranit kontakt, je možné odstranit pouze kontakty, které jste vytvořili.

## <a name="vendor-collaboration-user-requests"></a>Uživatelské žádosti dodavatelské spolupráce
Požadavky na uživatele dodavatelské spolupráce může zvýšit profesionál na nákup nebo správce externího dodavatele.

-   Pokud jste externího dodavatele, odeslání žádosti **všechny kontakty** stránky v rámci **spolupráce dodavatele** modulu.
-   Pokud jste odborník na nákup, odesíláte požadavky ze stránky **Zobrazit kontakty**. Provedete to tak, na záznam dodavatele, v **nastavení** části v podokně akcí vyberte **kontakty**&gt;**zobrazit kontakty**.

Lze vytvořit požadavek na zřízení uživatele, na deaktivaci uživatele nebo na změnu rolí zabezpečení Pokud jste správce externího dodavatele, musíte být registrováni jako kontaktní osoba pro účty dodavatele, pro které chcete vytvořit požadavky uživatelů a musíte mít přístup k rozhraní dodavatelské spolupráce pro tyto účty dodavatele.  

Když je odeslán požadavek, je přidán do seznamu **Žádosti uživatelů o dodavatelskou spolupráci** v modulu **Dodavatelská spolupráce** modulu a do seznamu **Požadavek uživatele dodavatelské spolupráce** v modulu **Nákup a zdroje** (Modul Nákup a zdroje není přístupný externím uživatelům).

### <a name="provision-a-user"></a>Zřízení uživatele

Předtím, než můžete požadovat zřízení nového uživatele, musí být tento uživatel nastaven jako kontakt pro jeden nebo více účtů dodavatele. Vytvoření žádosti o nového uživatele dodavatelské spolupráce:

1.  Na **všechny kontakty** klepněte na tlačítko **poskytnutí dodavatelského uživatele**.
2.  Zadejte e-mailovou adresu uživatele. Uživatel bude tuto adresu používat pro přihlášení do Dynamics 365 for Operations. Pokud e-mailová adresa patří do domény, která je registrována jako tenant v Microsoft Azure, musí být e-mailová adresa existující účte Azure Active Directory (ADD), aby byl proces zřizování úspěšně dokončen. Pokud e-mailová adresa nepatří k doméně registrované službou Microsoft Azure, přidaný účet bude vytvořen jako součást procesu zřizování a nový uživatel obdrží e-mail s pozváním. Příjemce e-mailové adresy domén jako @hotmail.com, @gmail.com, nebo @comcast.netnelze použít k registraci Dynamics 365 pro uživatelské operace.
3.  Nastavte možnost na **Povolený přístup k dodavatelské spolupráci na** **Ano** pro všechny právnické osoby, ke kterým musí mít uživatel přístup.
4.  V oddílu **Přiřazení rolí uživatelů** zaškrtněte políčko **Přiřadit** pro role zabezpečení, které by měl mít nový uživatel.
5.  Klepněte na tlačítko **Odeslat**.

Po odeslání požadavku uživatele dodavatele **povoleného přístupu spolupráce dodavatele** pole je nastavena na **Ano** u vybraného účtu dodavatele a uživatele požádat o zahájení pracovního postupu. V rámci tohoto workflowu je v Dynamics 365 for Operations vytvořen nový uživatel a přirazeny role zabezpečení. Kromě toho se aktivuje služba Azure B2B, která iniciuje interakci s portálem Azure a přidruží nový nebo existující účet AAD k uživatelskému účtu Dynamics 365 for Operations.

### <a name="inactivate-a-user"></a>Deaktivace uživatele

Odebrání přístupu uživatele dodavatele spolupráce lze provést dvěma způsoby:

-   Na stránce **Kontakty** pro dodavatele nastavte možnost **Přístup pro dodavatelskou spolupráci je povolen** na **Ne** pro kontakt. To lze provést jednotlivě podle právnických osob, pro které je osoba kontaktem. Tuto možnost mohou používat pouze odborníci na nákup.
-   Deaktivujte celý uživatelský účet odesláním požadavku **Deaktivovat dodavatelského uživatele**.

Požadovat, aby uživatel je deaktivován:

1.  Na **všechny kontakty** klepněte na tlačítko **deaktivaci****dodavatelského uživatele**.
2.  Do pole **Obchodní odůvodnění** napište komentář.
3.  Klepněte na tlačítko **Odeslat**.

### <a name="modify-security-roles"></a>Změna rolí zabezpečení

**Spravovat role uživatelů dodavatele** stránky je stejné jako **poskytnutí dodavatelského uživatele** stránky s výjimkou, že lze upravovat seznam rolí zabezpečení.  

Požadovat, aby role zabezpečení jsou upraveny pro uživatele:

1.  Na **všechny kontakty** klepněte na tlačítko **zachovat****role uživatele dodavatele**.
2.  Do pole **Obchodní odůvodnění** napište komentář.
3.  V části **Spravovat uživatelské role** zaškrtněte políčko u rolí zabezpečení, které chcete přiřadit, nebo zrušte zaškrtnutí políček u rolí, které chcete odstranit.
4.  Click **Submit**.





