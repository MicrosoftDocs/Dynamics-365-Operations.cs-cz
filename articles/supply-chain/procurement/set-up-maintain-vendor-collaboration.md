---
title: Nastavení a správa dodavatelské spolupráce
description: Toto téma vysvětluje, jak nastavit spolupráci dodavatele v Dynamics 365 Supply Chain Management. Vysvětluje také, jak zřídit nové uživatele pro spolupráci s dodavateli a spravovat role zabezpečení pro tyto uživatele.
author: Henrikan
ms.date: 12/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DirExternalRole, SysUserRequestListPage, VendVendorPortalUsers, WorkflowTableListPageRnr
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: 220774
ms.assetid: 69d05e8b-7dc2-48ea-bc24-bea9ac963579
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b635255fffa6fd3c6612cd248dc692df204aa76d
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/19/2021
ms.locfileid: "7651951"
---
# <a name="set-up-and-maintain-vendor-collaboration"></a>Nastavení a správa dodavatelské spolupráce

[!include [banner](../includes/banner.md)]

Rozhraní pro spolupráci s dodavateli nabízí omezené informace o nákupních objednávkách, fakturách a skladových zásobách pro uživatele externích dodavatelů. Z tohoto rozhraní může dodavatel také odpovídat na žádosti o cenovou nabídku (RFQ) a zobrazovat a upravovat základní informace o společnosti.

Toto téma vysvětluje, jak nastavit spolupráci dodavatele v Dynamics 365 Supply Chain Management. Vysvětluje také, jak nastavit pracovní postup ke zřízení nových uživatelů pro spolupráci s dodavateli a jak spravovat role zabezpečení pro tyto uživatele.

> [!NOTE]
> Informace o nastavení rolí zabezpečení pro spolupráci s dodavateli platí pouze pro aktuální verzi Finance and Operations. V aplikaci Microsoft Dynamics AX 7.0 (únor 2016) a Microsoft Dynamics AX 7.0.1 (květen 2016) můžete spolupracovat s dodavateli pomocí modulu **Portál pro dodavatele**. Informace o uživatelských oprávněních pro portál dodavatele v Microsoft Dynamics AX viz [Zabezpečení uživatele portálu dodavatele](configure-security-vendor-portal-users.md).

## <a name="set-up-vendor-collaboration-security-roles"></a>Nastavení rolí zabezpečení dodavatelské spolupráce

Odborník na nákup nebo dodavatel, který má dostatečná oprávnění, může povolením požádat o zřízení kontaktní osoby jako uživatele aktivací **Zřídit uživatele poskytovatele** v záznamu kontaktní osoby. Během procesu zřizování se pro nového externího uživatele vyberou uživatelská oprávnění a odešle se požadavek nového uživatele dodavatele. Je důležité, abyste správně nastavili uživatelská oprávnění, která jsou k dispozici pro výběr v požadavku uživatele dodavatele. V opačném případě by dodavatelům mohl být udělen přístup k informacím, ke kterým by neměli mít přístup v rámci Supply Chain Management.

### <a name="set-up-the-security-roles-that-are-available-for-selection-when-a-new-user-request-is-used-for-a-contact-person"></a>Nastavte role zabezpečení, které jsou k dispozici pro výběr, když je pro kontaktní osobu použit nový požadavek uživatele

1. Vyberte **Správa systému** &gt; **Zabezpečení** &gt; **Externí role**.
2. Vyberte **Nový** a poté vyberte roli zabezpečení a roli strany **Prodejce**.

Možná budete chtít přidat role **Správce dodavatele (externí)** a **Prodejce (externí)**, které jsou poskytovány v Supply Chain Management. Případně můžete použít role zabezpečení, které vaše společnost vytvořila.

Měli byste roli **Správce dodavatele (externí)** zpřístupnit pouze v případě, že by dodavatelé měli být schopni vytvářet nové kontakty, odesílat požadavky uživatelů na spolupráci s dodavateli pro nové uživatele a změny informací o uživatelích a zpracovávat tyto požadavky prostřednictvím pracovního postupu.

Pokud plánujete ručně nastavit kontakty a uživatele dodavatele, můžete zpřístupnit pouze **roli Dodavatel (externí)**. Tato role pak bude jedinou rolí, kterou lze vyžádat prostřednictvím požadavku uživatele dodavatele.

> [!NOTE]
> Role **SystemUser** je automaticky přidělena, když ručně vytvoříte nový účet uživatele. Proto musíte tuto roli odebrat a přiřadit roli **SystemExternalUser**. Pokud jsou nové uživatelské účty vytvořeny prostřednictvím pracovního postupu, který je zahájen požadavkem uživatele dodavatele na poskytnutí nového uživatele, bude přidělena jedna nebo více rolí, které jste nastavili pro spolupráci s dodavatelem, a role **SystemExternalUser**.

#### <a name="vendor-admin-external-security-role"></a>Role zabezpečení správce dodavatele (externí)

Role **Správce dodavatele (externí)** může být použita pro externí dodavatele, kteří udržují kontaktní informace dodavatele a podávají požadavky na poskytování nových uživatelů spolupráce s dodavateli. Externí uživatelé, kteří mají tuto roli zabezpečení, mohou provádět následující úlohy:

- Zobrazení a úprava informací o kontaktní osobě, jako je titul, e-mailová adresa a telefonní číslo osoby.
- Přidání nové nebo existující kontaktní osoby k účtům dodavatelů, pro které jsou kontaktem.
- Odstranění všech kontaktních osob, které vytvořili.
- Aktivace nebo deaktivace spojení mezi kontaktní osobou a účtem dodavatele. Poté, co je spojení mezi kontaktní osobou a účtem dodavatele deaktivováno, nelze na kontaktní osobu odkazovat v nových nákupních objednávkách nebo jiných dokumentech.
- Odepření nebo aktivace přístupu kontaktní osoby k dokumentům na rozhraní spolupráce s dodavatelem, které jsou specifické pro účet dodavatele. Po deaktivaci přidružení mezi kontaktní osobou a účtem dodavatele je vždy odepřen přístup k dokumentům, které jsou specifické pro účet dodavatele.
- Žádost o nový uživatelský účet pro kontaktní osobu pomocí akce **Zřídit uživatele**.
- Požádat o deaktivaci uživatelského účtu kontaktní osoby.
- Požádat o úpravu uživatelského účtu kontaktní osoby za účelem přidání nebo odebrání rolí zabezpečení.
- Zobrazovat požadavky na nabídku.

#### <a name="vendor-external-security-role"></a>Role zabezpečení dodavatel (externí)

**Roli Dodavatel (externí)** lze použít pro externí dodavatele, kteří budou pracovat s nákupními objednávkami. Externí uživatelé, kteří mají tuto roli zabezpečení, mohou provádět následující úlohy:

- Odpovídat a zobrazovat informace o nákupních objednávkách.
- Udržovat faktury dodavatelské spolupráce.
- Zobrazit zásoby dodávky.
- Zobrazit a reagovat na žádost o nabídku.
- Prohlížet informace o dodavateli.

## <a name="set-up-security-roles-that-are-used-when-prospective-vendors-are-onboarded"></a>Nastavení rolí zabezpečení, které se použijí při začlenění potenciálních dodavatelů

Chcete-li integrovat dodavatele, kteří jsou iniciováni prostřednictvím žádosti o registraci potenciálního dodavatele, musíte nastavit externí roli zabezpečení. Tato role bude přiřazena novým uživatelům během procesu zřizování, který je řízen pracovním postupem typu **Pracovní postup požadavků uživatele (platforma)**. Pro více informací viz část [Nastavení pracovních postupů pro zpracování požadavků uživatelů na spolupráci s dodavateli](#set-up-workflows-to-process-vendor-collaboration-user-requests) dále v tomto tématu.

Informace o tom, jak zapojit potenciální dodavatele, viz [Zapojení dodavatelů](vendor-onboarding.md).

### <a name="set-up-a-security-role-that-is-used-when-a-new-prospective-vendor-user-request-is-submitted"></a>Nastavte roli zabezpečení, která se použije při odeslání nového požadavku uživatele potenciálního dodavatele

1. Vyberte **Správa systému** > **Zabezpečení** > **Externí role**.
2. Vyberte **Nový** a poté vyberte roli zabezpečení a roli strany **Potenciální dodavatel**.

Měli byste přidat roli **Potenciální dodavatel (externí)**, která je poskytována v Supply Chain Management.

Role zabezpečení udělí přístup pouze novému průvodci registrací dodavatele.

## <a name="set-up-workflows-to-process-vendor-collaboration-user-requests"></a>Nastavení pracovních postupů pro zpracování požadavků uživatelů na spolupráci s dodavateli

Chcete-li zaručit, že budou provedeny všechny relevantní úkoly a že budou udělena příslušná schválení, musíte nastavit pracovní postupy pro zpracování požadavků uživatelů na spolupráci s dodavateli.

Požadavky uživatelů na spolupráci dodavatelů jsou odesílány buď externími dodavateli, kteří mají roli zabezpečení **Správce dodavatele (externí)** nebo podobná oprávnění, nebo odborníky na nákup ve vaší společnosti. Mohou být také generovány z požadavků na registraci potenciálních dodavatelů během procesu registrace dodavatele.

Existují tři typy požadavků:

- Žádosti o zřízení nového uživatele
- Žádosti o deaktivaci stávajícího uživatele
- Požadavky na úpravu rolí zabezpečení stávajícího uživatele

Další informace o žádostech uživatelů o spolupráci s dodavateli viz téma [Správa uživatelů dodavatelské spolupráce](manage-vendor-collaboration-users.md).

Musíte vytvořit dva nebo více pracovních postupů pro zpracování všech tří typů požadavků uživatelů na spolupráci s dodavateli. Nové pracovní postupy jsou vytvářeny na stránce **Uživatelské pracovní postupy**.

### <a name="example-of-a-workflow-for-provisioning-new-users-and-modifying-security-roles"></a>Příklad pracovního postupu pro zřizování nových uživatelů a úpravu rolí zabezpečení

Chcete-li zpracovat požadavky uživatelů dodavatele na vytvoření nových uživatelů a úpravu rolí zabezpečení, můžete na začátek pracovního postupu umístit podmínku větvení. Tímto způsobem se používá jiná větev pracovního postupu v závislosti na tom, zda je požadavek na vytvoření nového uživatele, nebo na úpravu stávajícího uživatele.

Chcete-li nastavit toto větvení, vytvořte nový pracovní postup typu **Pracovní postup požadavku uživatele (platforma)**. Větve tohoto pracovního postupu mohou obsahovat následující prvky.

#### <a name="branch-to-provision-new-users"></a>Větvení pro zřizování nových uživatelů

1. Přidělte úkol schvalování osobě, která je odpovědná za schvalování, že novým uživatelům by měl být udělen přístup k informacím o spolupráci dodavatele.
2. Přidělte úkol osobě, která je zodpovědná za žádost o nové uživatelské účty Microsoft Azure Active Directory (Azure AD) v Azure Portal. Použijte předdefinovaný úkol **Odeslat pozvánku pro uživatele Azure B2B** pro tento krok. B2B uživatelé mohou být automaticky exportováni do Azure AD. Použijte předdefinované **Zřídit uživatele Azure AD B2B**. Více informací viz [Export B2B uživatelů do Azure AD](../../fin-ops-core/dev-itpro/sysadmin/implement-b2b.md).
3. Přidělte úkol schválení osobě, která nahrává do Azure. Pokud se účet úspěšně nevytvoří, tato osoba úkol odmítne a ukončí pracovní postup. Tento úkol schvalování lze přeskočit, pokud jste zahrnuli krok, který automaticky exportuje nové uživatelské účty do Azure přes B2B aplikační programovací rozhraní (API).
4. Přidejte automatizovanou úlohu, která zřídí nového uživatele. Použijte předdefinovaný úkol **Automatické zřízení uživatele** pro tento krok.
5. Přidejte úlohu, která upozorní nového uživatele. Možná budete chtít poslat novému uživateli uvítací e-mail, který bude obsahovat URL pro Supply Chain Management. Tento e-mail může používat šablonu, kterou vytvoříte na stránce **E-mailové zprávy** a poté vyberte na stránce **Parametry pracovního postupu uživatele**. Šablona může obsahovat štítek **%portalURL%**. Když je vygenerován uvítací e-mail, tato značka bude nahrazena adresou URL klienta Supply Chain Management.

    > [!NOTE]
    > Tento pracovní postup lze použít ve více scénářích, které zahrnují registraci uživatele. Lze jej například použít, když potenciální dodavatelé nebo kontaktní osoby vyžadují účet pro spolupráci s dodavatelem. Proto byste měli e-mail formulovat jako obecné prohlášení, které lze použít pro různé účely.

#### <a name="branch-to-modify-security-roles"></a>Větvení pro úpravu rolí zabezpečení

1. Přidělte úkol schvalování osobě, která je odpovědná za schvalování změn rolí zabezpečení.
2. Přidejte automatizovanou úlohu, která přidá nebo odebere relevantní role zabezpečení. Použijte úkol **Automatické zřízení uživatele** pro tento krok.

### <a name="example-of-a-workflow-for-inactivating-a-user"></a>Příklad pracovního postupu pro deaktivaci uživatele

Vytvořte pracovní postup typu **Deaktivovat platformu pracovního postupu požadavků uživatele** a poté přidejte následující úkoly.

1. Přidělte úkol schvalování osobě, která je odpovědná za přijímání požadavků k deaktivaci uživatelů. Chcete-li tento krok schvalování automatizovat, můžete přidat podmínky.
2. Přidejte automatizovanou úlohu, která deaktivuje uživatele. Použijte úkol **Automatická deaktivace uživatele** pro tento krok.
3. Přidejte všechny požadované úkoly čištění. Můžete například přidat úlohu, která odebere účet z vašeho adresáře v Azure Portal.

## <a name="enable-vendor-collaboration-for-a-specific-vendor"></a>Aktivace spolupráce pro konkrétního dodavatele

Před vytvořením uživatelského účtu pro někoho, kdo bude používat spolupráci dodavatele, musíte nastavit dodavatele, aby mohl používat dodavatelskou spolupráci. Na stránce **Dodavatelé** na kartě **Obecné** nastavte pole **Aktivace spolupráce**. Existují tyto možnosti:

- **Aktivní (nákupní objednávky je automaticky potvrzena)** – nákupní objednávky se automaticky potvrzují poté, co je dodavatel přijme beze změn.
- **Aktivní (nákupní objednávka není automaticky potvrzena)** – nákupní objednávky musí být ručně potvrzeny vaší organizací poté, co je dodavatel přijal.

> [!NOTE]
> Tento úkol mohou splnit i odborníci na nákup ve vaší společnosti.

## <a name="troubleshoot-the-provisioning-of-new-vendor-collaboration-users"></a>Odstraňování problémů s poskytováním nových uživatelů spolupráce s dodavateli

Noví uživatelé spolupráce s dodavateli jsou zřízeni prostřednictvím pracovního postupu, který jste nastavili pro zpracování požadavků uživatelů na spolupráci s dodavatelem typu **Zřídit dodavatelského uživatele**.

Pokud e-mailová adresa nového uživatele pro spolupráci s dodavatelem patří do domény, která je v Azure registrována jako klient (tedy pokud se jedná o účet spravované domény), e-mailová adresa musí být existující účet Azure AD. V opačném případě nelze proces zřizování dokončit.

Další informace o procesu, který se používá v úloze **Odeslat pozvánku pro uživatele Azure B2B** v pracovním postupu pro správu účtu Azure AD viz [B2B spolupráce Azure Active Directory](/azure/active-directory/external-identities/what-is-b2b).

## <a name="additional-resources"></a>Další prostředky

[Dodavatelská spolupráce s externími dodavateli](vendor-collaboration-work-external-vendors.md)

Podívejte se na krátké video o procesu registrace dodavatele: [Registrace nového dodavatele](https://www.youtube.com/watch?v=0KUc3AGaTKk&feature=youtu.be)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
