---
title: Integrace s LinkedIn Talent Hub
description: Toto téma vysvětluje, jak nastavit integraci mezi Microsoft Dynamics 365 Human Resources a LinkedIn Talent Hub.
author: jaredha
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d14a8cb1973e0ed55ef10ddb43415eba80eb5c1b
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717104"
---
# <a name="integrate-with-linkedin-talent-hub"></a>Integrace s LinkedIn Talent Hub

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

> [!IMPORTANT]
> Integrace mezi Dynamics 365 Human Resources a LinkedIn Talent Hub popsané v tomto tématu byly 31. prosince 2021 vyřazeny. Integrační služba po tomto datu již nebude k dispozici. Organizace, které dosud nepoužívají integrační službu, nebudou moci tuto službu implementovat před vyřazením.

[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) je platforma pro systém sledování žadatelů (ATS). Umožňuje vám získávat, spravovat a najímat zaměstnance z jednoho místa. Integrací Microsoft Dynamics 365 Human Resources s LinkedIn Talent Hub můžete snadno vytvářet záznamy o zaměstnancích v Human Resources pro uchazeče, kteří byli najati na pozici.

## <a name="setup"></a>Nastavení

Nastavení integrace s LinkedIn Talent Hub musí provést správce systému. Nejprve v prostředí Power Apps musíte nastavit uživatele a roli zabezpečení, abyste LinkedIn Talent Hub udělili příslušná oprávnění k zápisu dat do Human Resources.

### <a name="link-your-environment-to-linkedin-talent-hub"></a>Propojte své prostředí s LinkedIn Talent Hub

1. Otevřete [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).

2. V rozevírací nabídce uživatele vyberte možnost **Nastavení produktu**.

3. V levém navigačním podokně v sekci **Rozšířené** vyberte **Integrace**.

4. Vyberte **Autorizovat** pro integraci Microsoft Dynamics 365 Human Resources.

5. Na stránce **Dynamics 365 Human Resources** vyberte prostředí, ke kterému chcete propojit LinkedIn Talent Hub, a poté vyberte **Propojit**.

    ![Zprovoznění LinkedIn Talent Hub.](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > Můžete se připojit pouze k prostředím, kde má váš uživatelský účet přístup správce do prostředí Human Resources i do přidruženého prostředí Power Apps. Pokud na stránce propojení s Human Resources nejsou uvedena žádná prostředí, ujistěte se, že máte v klientovi licencovaná prostředí Human Resources a že uživatel, pod kterým jste se přihlásili ke stránce s propojením, má oprávnění správce jak do prostředí Human Resources, tak do prostředí Power Apps.

### <a name="create-a-power-apps-security-role"></a>Vytvoření role zabezpečení Power Apps

1. Otevřete [centrum pro správu Power Platform](https://admin.powerplatform.microsoft.com).

2. V seznamu **Prostředí** vyberte prostředí přidružené k prostředí Human Resources, se kterým chcete propojit instanci LinkedIn Talent Hub.

3. Vyberte **Nastavení**.

4. Rozbalte uzel **Uživatelé + oprávnění** a vyberte **Role zabezpečení**.

5. Na stránce **Role zabezpečení** vyberte **Nová role**.

6. Na kartě **Podrobnosti** zadejte název role, například **Integrace LinkedIn Talent Hub HRIS**.

7. Na kartě **Vlastní nastavení** vyberte na úrovni organizace oprávnění **Čtení** pro následující entity:

    - Entita
    - Pole
    - Vztah

8. Uložte a zavřete roli zabezpečení.

### <a name="create-a-power-apps-application-user"></a>Vytvoření uživatele aplikace Power Apps

Pro adaptér LinkedIn Talent Hub musí být vytvořen uživatel aplikace, aby byla adaptéru udělena oprávnění k zápisu záznamů kandidátů do prostředí Power Apps.

1. Otevřete [centrum pro správu Power Platform](https://admin.powerplatform.microsoft.com).

2. V seznamu **Prostředí** vyberte prostředí přidružené k prostředí Human Resources, se kterým chcete propojit instanci LinkedIn Talent Hub.

3. Vyberte **Nastavení**.

4. Rozbalte uzel **Uživatelé + oprávnění** a vyberte možnost **Uživatelé**.

5. Vyberte **Spravovat uživatele v Dynamics 365**.

6. V rozevírací nabídce nad seznamem můžete změnit zobrazení z výchozího **Povolení uživatelé** na **Uživatelé aplikace**.

    ![Zobrazení Uživatelé aplikace.](./media/hr-admin-integration-power-apps-application-users.jpg)

7. Na panelu nástrojů vyberte **Nový**.

8. Na stránce **Nový uživatel** proveďte následující kroky:

    1. Změňte hodnotu pole **Typ uživatele** na **Uživatel aplikace**.
    2. Nastavte pole **Uživatelské jméno** na **Integrace Dynamics365 HR LinkedIn HRIS**.
    3. Nastavte pole **ID aplikace** na **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.
    4. Zadejte libovolnou hodnotu do polí **Křestní jméno**, **Příjmení** a **Primární e-mail**.
    5. Na panelu nástrojů vyberte **Uložit a zavřít**.

### <a name="assign-a-security-role-to-the-new-user"></a>Přiřazení role zabezpečení novému uživateli

Po uložení a zavření nového uživatele aplikace v předchozí části jste se vrátili na stránku **Seznam uživatelů**.

1. Na stránce **Seznam uživatelů** změňte zobrazení na **Uživatelé aplikace**.

2. Vyberte uživatele aplikace, kterého jste vytvořili v předchozí části.

3. Na panelu nástrojů vyberte **Správa rolí**.

4. Vyberte roli zabezpečení, kterou jste vytvořili dříve pro integraci.

5. Vyberte **OK**.

### <a name="add-an-azure-active-directory-app-in-human-resources"></a>Přidání aplikace Azure Active Directory v Human Resources

1. V Dynamics 365 Human Resources otevřete stránku **Aplikace Azure Active Directory**.
2. Přidejte nový záznam do seznamu a nastavte následující pole:

    - **ID klienta**: Zadejte **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.
    - **Název**: Zadejte název role zabezpečení Power Apps, kterou jste vytvořili dříve, například **Integrace LinkedIn Talent Hub HRIS**.
    - **ID uživatele**: Vyberte uživatele, který má oprávnění k zápisu dat do pracovního prostoru Správa zaměstnanců.

### <a name="create-the-table-in-dataverse"></a>Vytvoření tabulky v Dataverse

> [!IMPORTANT]
> Integrace s LinkedIn Talent Hub závisí na virtuálních tabulkách v Dataverse pro Human Resources. Jako předpoklad pro tento krok musíte v nastavení nakonfigurovat virtuální tabulky. Informace o konfiguraci virtuálních tabulke najdete v tématu [Konfigurace virtuálních tabulek Dataverse](./hr-admin-integration-common-data-service-virtual-entities.md).

1. V Human Resources otevřete stránku **Integrace Dataverse**.

2. Vyberte kartu **Virtuální tabulky**.

3. Filtrujte seznam entit podle popisku entity a vyhledejte **Exportovaný kandidát LinkedIn**.

4. Vyberte entitu a poté vyberte možnost **Generovat/aktualizovat**.

## <a name="exporting-candidate-records"></a>Export záznamů kandidátů

Po dokončení nastavení mohou pracovníci náboru a odborníci na personalistiku (HR) používat funkci **Export to HRIS** (Exportovat do HRIS) v LinkedIn Talent Hub pro export záznamů přijatých kandidátů z LinkedIn Talent Hub do Human Resources.

### <a name="export-records-from-linkedin-talent-hub"></a>Export záznamů z LinkedIn Talent Hub

Poté, co kandidát prošel náborovým procesem a byl přijat, můžete exportovat záznam kandidáta z LinkedIn Talent Hub do Human Resources.

1. V LinkedIn Talent Hub otevřete projekt, pro který jste nového zaměstnance najali.

2. Vyberte záznam kandidáta.

3. Vyberte **Change state** (Změnit stav) a poté vyberte **Hired** (Zařazen).

4. V nabídce se třemi tečkami (**...**) pro kandidáta vyberte **Export to HRIS** (Exportovat do HRIS).

5. V podokně **Export do HRIS** zadejte informace, které je třeba exportovat:

    - V poli **HRIS provider** (Poskytovatel HRIS) vyberte **Microsoft Dynamics 365 Human Resources**.
    - V poli **Start date** (Počáteční datum) vyberte hodnotu pro nového zaměstnance.
    - V poli **Job title** (Pracovní pozice) zadejte název pozice nového zaměstnance.
    - V poli **Location** (Umístění) zadejte umístění, kde bude zaměstnanec sídlit.
    - Zadejte nebo ověřte e-mailovou adresu zaměstnance.

![Export do podokna HRIS v LinkedIn Talent Hub.](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a>Dokončení zprovoznění v Human Resources

Záznamy kandidátů, které jsou exportovány z LinkedIn Talent Hub do Human resources, se objeví v sekci **Uchazeči o pracovní místo** na stránce **Správa zaměstnanců**.

1. V Human Resources otevřete stránku **Správa zaměstnanců**.

2. V sekci **Uchazeči o pracovní místo** vyberte **Zařadit** pro vybraného kandidáta.

3. V dialogovém okně **Přijmout nového pracovníka** zkontrolujte záznam a přidejte všechny požadované informace. Můžete také vybrat číslo pozice, na kterou byl kandidát přijat.

Po zadání požadovaných informací můžete pokračovat ve standardních procesech pro vytváření záznamů zaměstnanců a nabírání zaměstnanců.

Následující údaje se importují a zahrnou do nového záznamu zaměstnance:

- Křestní jméno
- Příjmení
- Počáteční datum zaměstnání
- E-mailová adresa
- Telefonní číslo

## <a name="see-also"></a>Viz také

[Konfigurace virtuálních tabulek Dataverse](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Co je Microsoft Dataverse?](/powerapps/maker/common-data-service/data-platform-intro)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
