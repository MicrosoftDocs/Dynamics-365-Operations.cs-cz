---
title: Ověření mezi servery pro integrační API ATS
description: Toto téma popisuje, jak nastavit ověřování mezi servery pro integraci proti rozhraní API integrace Dynamics 365 Human Resources Applicant Tracking System (ATS).
author: jaredha
ms.date: 06/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-06-30
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d221e1a47dca85880fd683177ca95dd1b7766fb9
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8064915"
---
# <a name="server-to-server-authentication-for-the-ats-integration-api"></a>Ověření mezi servery pro integrační API ATS


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma popisuje, jak nastavit ověřování mezi servery pro integrace aplikace proti rozhraní API integrace Dynamics 365 Human Resources Applicant Tracking System (ATS). Existuje několik vrstev zabezpečení, které je třeba spravovat, aby instanční objekt získal přístup k virtuální tabulce Microsoft Dataverse a souvisejícím datům. Uživateli musí být udělen přístup k virtuální tabulce Dataverse v Microsoft Power Platform a přístup k datům v Dynamics 365 Human Resources.

## <a name="enable-access-to-dataverse-virtual-tables-in-power-platform"></a>Povolení přístupu k virtuálním tabulkám Dataverse v Power Platform

První krok umožnění přístupu k virtuálním tabulkám Dataverse v Power Platform je nastavit vaši aplikaci v Power Platform pro autentizaci proti koncovým bodům virtuální tabulky Dataverse. Kroky k tomu jsou uvedeny v [průvodci pro vývojáře Microsoft Dataverse](/powerapps/developer/data-platform).

  - Pro registrace aplikací pro jednoho klienta: [Použijte ověřování typu server-klient pro jednoho klienta](/powerapps/developer/data-platform/use-single-tenant-server-server-authentication)
  - Pro registrace aplikací pro více klienta: [Použijte ověřování typu mezi servery pro více klientů](/powerapps/developer/data-platform/use-multi-tenant-server-server-authentication)

### <a name="creating-a-security-role-for-ats-integrations"></a>Vytvoření role zabezpečení pro integrace ATS

Jedním z kroků po vytvoření uživatele aplikace je přiřadit uživatele roli zabezpečení, která definuje přístup, který aplikace bude mít ke koncovým bodům. Toto je krok 7 ve [vytvoření uživatele aplikace](/powerapps/developer/data-platform/use-single-tenant-server-server-authentication#application-user-creation) pro registrace aplikací pro jednoho klienta a [vytvoření role zabezpečení pro uživatele aplikace](/powerapps/developer/data-platform/use-multi-tenant-server-server-authentication#create-a-security-role-for-the-application-user) pro registrace více klientů. 

Role, ke které přiřadíte uživatele aplikace, musí mít přístup k datovým entitám použitým pro vaši integraci ATS. Ta není ihned k dispozici, takže bude nutné vytvořit novou roli zabezpečení. Novou roli lze vytvořit podle kroků uvedených v části [Vytvoření role zabezpečení](/power-platform/admin/create-edit-security-role#create-a-security-role).

U nové role musí být odpovídající přístup přiřazen minimálně následujícím entitám na kartě **Vlastní entity** nové role. Mohou existovat další entity, které budete muset přidat, pokud integrace používá rozsáhlejší data aplikace. Po vytvoření nové role ji lze přiřadit uživateli aplikace.

  - Základní pracovník (mshr)
  - Kandidát k přijetí (mshr)
  - Certifikát o dovednosti (mshr)
  - Typ certifikátu (mshr)
  - Společnost
  - Pracovní funkce kompenzace (mshr)
  - Typ úlohy kompenzace (mshr)
  - Země/oblasti (mshr)
  - Oddělení (mshr)
  - Vzdělávací kompetence (mshr)
  - Stupeň vzdělání (mshr)
  - Obory vzdělání (mshr)
  - Požadavky na vzdělání (mshr)
  - Identifikace (mshr)
  - Typ identifikace (mshr)
  - Instituce (mshr)
  - Vydávající úřad (mshr)
  - Kompenzace úlohy (mshr)
  - Pracovní místa (mshr)
  - Úroveň vzdělání (mshr)
  - Kontakty strany (mshr)
  - Lidé (mshr)
  - Adresy osob (mshr)
  - Prověřování osoby (mshr)
  - Typ pozice (mshr)
  - Pozice V2 (mshr)
  - Kompetence odborné praxe (mshr)
  - Úroveň hodnocení (mshr)
  - Modely hodnocení (mshr)
  - Kódy důvodů (mshr)
  - Požadavek na nábor (mshr)
  - Požadavek na nábor – místo (mshr)
  - Požadavek na nábor – pozice (mshr)
  - Požadavek na nábor – dovednosti (mshr)
  - Typy prověřování (mshr)
  - Dovednostní kompetence (mshr)
  - Dovednosti (mshr)
  - Tituly (mshr)
  - Status veterána (mshr)
  - Pracovník (mshr)

## <a name="granting-application-permissions-to-human-resources-data"></a>Udělení oprávnění aplikace k datům Human Resources

Druhým krokem je zajistit, aby aplikaci byla udělena příslušná oprávnění k datům v Human Resources propojením s uživatelem v aplikaci Human Resources. U uživatele aplikace jsou volání mezi servery prostřednictvím virtuálních tabulek Dataverse prováděny v kontextu identity uživatele (aplikace) v Dataverse, které vyvolává akci. Služba adaptéru virtuální tabulky poté vyhledá přidruženého uživatele v Human Resources a spustí dotaz v kontextu daného uživatele. To znamená, že uživatel musí být vytvořen v Human Resources se správnými přiřazenými rolemi, aby mohl poskytnout přístup k datům, která bude integrace potřebovat.

Uživateli Human Resources bude také nutné přiřadit správná oprávnění k datům v oblasti Human Resources. Role **Žádost o nábor** (HcmRecruitingIntegrator) je k dispozici s oprávněními pro primární entity potřebné pro integraci s náborovými daty. Tuto roli lze přiřadit uživateli aplikace na stránce **Uživatelé** k udělení příslušného přístupu k údajům. Další informace o rolích zabezpečení Human Resources najdete v tématu [Zabezpečení založené na rolích](/fin-ops-core/dev-itpro/sysadmin/role-based-security).

### <a name="set-up-the-new-user-with-appropriate-permissions"></a>Nastavení nového uživatele s příslušnými oprávněními

K nastavení nového uživatele s příslušnými oprávněními postupujte následovně:

  1. Otevřete stránku **Uživatelé** stránku v Human Resources a vyberte **Nový**.
  2. Zadejte **ID uživatele** a **Uživatelské jméno** pro nového uživatele aplikace. Můžete například zadat „RecruitingIntegration“.

      > [!NOTE]
      > Pokud aplikace nemá uživatelský účet nebo e-mailovou adresu Microsoft Azure Active Directory (Azure AD), můžete do polí e-mailová adresa a poskytovatel pro uživatele zadat něco jako „RecruitingApp“.

  3. Na pevné záložce **Role uživatele** vyberte akci **Přiřadit role**.
  4. V podokně **Přiřadit role uživateli** vyberte **Aplikace náboru** a vyberte **OK**.
  5. Uložte nový záznam uživatele.

### <a name="link-the-new-human-resources-user-to-the-application"></a>Propojení nového uživatele Human Resources s aplikací

Po vytvoření uživatele musí být pro aplikaci vytvořen záznam ve formuláři **Aplikace Azure Active Directory** pro propojení aplikace s uživatelem Human Resources.

  1. Otevřete formulář **Aplikace Azure Active Directory** a vyberte **Nový**.
  2. Do pole **ID klienta** zadejte ID klienta uživatele aplikace vytvořeného pro aplikaci.
  3. Do pole **Název** zadejte název aplikace integrace.
  4. V poli **ID uživatele** vyberte nového uživatele Human Resources vytvořeného pro integraci náboru.
  5. Uložte nový záznam.

Aplikace pak bude mít přístup k údajům Human Resources, omezeným pouze na údaje potřebné pro integraci aplikace náboru.

## <a name="see-also"></a>Viz také

[Nábor uchazečů o práci](hr-personnel-recruit.md)<br>
[Co je Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Použití webového rozhraní Microsoft Dataverse Web API](/powerapps/developer/data-platform/webapi/overview)<br>
[Vytváření a aktualizace sad možností pomocí webového rozhraní API](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
