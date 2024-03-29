---
title: Kopírovat instanci
description: Pomocí služby Microsoft Dynamics Lifecycle Services (LCS) můžete kopírovat databázi Microsoft Dynamics 365 Human Resources do prostředí izolovaného prostoru (sandbox).
author: twheeloc
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 20a2ffb44f9b99800146e3365e6f0d6df8e9a75e
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324253"
---
# <a name="copy-an-instance"></a>Kopírovat instanci

_**Platí pro:** Human Resources na samostatné infrastruktuře_ 

> [!NOTE]
> Od června 2022 lze prostředí Human Resources nasadit pouze na infrastrukturu finančních a provozních aplikací. Více informací viz [Zřízení Human Resources ve finanční a provozní infrastruktuře](hr-admin-setup-provision-fo.md).

> [!IMPORTANT]
> Finanční a provozní infrastruktura nepodporuje funkci instance kopírování. Můžete nasadit nová prostředí a používat databázové pohyby k vytváření kopií. Další informace o samoobslužných nasazení viz [Přehled samoobslužného nastavení](../fin-ops-core/dev-itpro/deployment/infrastructure-stack.md). Další informace o pohybech databáze na finanční a provozní infrastruktuře viz [Úvodní stránka operací pohybu databáze](../fin-ops-core/dev-itpro/database/dbmovement-operations.md).

Pomocí služby Microsoft Dynamics Lifecycle Services (LCS) můžete kopírovat databázi Microsoft Dynamics 365 Human Resources do prostředí izolovaného prostoru (sandbox). Máte-li jiné prostředí izolovaného prostoru (sandbox), můžete také zkopírovat databázi z prostředí do cíleného prostředí sandbox.

Při kopírování instance mějte na paměti následující tipy:

- Instance aplikace Human Resources, kterou chcete přepsat, musí být prostředí izolovaného prostoru (sandbox).

- Prostředí, ze kterých a do kterých kopírujete, musí být ve stejné oblasti. Nelze kopírovat mezi oblastmi.

- Musíte být správcem cílového prostředí, abyste se k němu mohli po zkopírování instance přihlásit.

- Při kopírování databáze aplikace Human Resources nejsou zkopírovány prvky (aplikace nebo data), které jsou obsaženy v prostředí Microsoft Power Apps. Informace o tom, jak kopírovat prvky do prostředí Power Apps, naleznete v tématu [kopírování prostředí](/power-platform/admin/copy-environment). Prostředí Power Apps, které chcete přepsat, musí být prostředí izolovaného prostoru (sandbox). Chcete-li změnit produkční prostředí Power Apps na prostředí s izolovaným prostorem, musíte být globálním správcem klienta. Další informace o změně prostředí Power Apps naleznete v tématu [přepnutí instance](/dynamics365/admin/switch-instance).

- Pokud zkopírujete instanci do prostředí sandbox a chcete integrovat prostředí sandbox s Dataverse, musíte znovu použít vlastní pole na tabulky Dataverse. Viz [Použití vlastních polí na Dataverse](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).

## <a name="effects-of-copying-a-human-resources-database"></a>Vliv kopírování databáze aplikace Human Resources

> [!Note]
> Od srpna 2022 budou dokumenty v Microsoft Azure Blob Storage je zahrnuto při kopírování produkčního prostředí do prostředí sandbox. Všechny dokumenty a šablony, které jsou připojeny, budou zkopírovány ze zdrojového prostředí do cílového prostředí.

Při kopírování databáze aplikace Human Resources dojde k následujícím událostem:

- Při kopírování bude existující databáze vymazána v cílovém prostředí. Po dokončení kopírování nelze stávající databázi obnovit.

- Cílové prostředí nebude k dispozici, dokud nebude proces kopírování dokončen.

- Všichni uživatelé s výjimkou těch, kteří mají roli zabezpečení „Správce systému“, a dalších uživatelských účtů interní služby, nebudou k dispozici. Správce může odstranit data před tím, než se budou moci ostatní uživatelé vrátit do systému.

- Každý uživatel s rolí zabezpečení „Správce systému“ musí provést požadované změny konfigurace, například znovu připojit koncové body integrace ke konkrétním službám nebo adresám URL.

## <a name="copy-the-human-resources-database"></a>Kopírování databáze aplikace Human Resources

Chcete-li dokončit tento úkol, nejprve zkopírujte instanci a poté se přihlaste do centra pro správu Microsoft Power Platform a zkopírujte vaše prostředí Power Apps.

> [!WARNING]
> Při kopírování instance je databáze vymazána v cílové instanci. Cílová instance není během tohoto procesu k dispozici.

1. Přihlaste se k LCS a vyberte projekt LCS obsahující instanci, kterou chcete zkopírovat.

2. Ve svém LCS projektu vyberte dlaždici **Správa aplikace Human Resources**.

3. Vyberte instanci, kterou chcete zkopírovat, a pak vyberte **Kopírovat**.

4. V podokně úloh **Kopírovat instanci** vyberte instanci, kterou chcete přepsat, a poté vyberte možnost **kopírovat**. Počkejte, až bude pole **Kopírovat stav** aktualizováno na hodnotu **dokončeno**.

   ![[Vyberte instanci, která má být přepsána.](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. Vyberte **Power Platform** a přihlaste se do centra pro správu Microsoft Power Platform.

   ![[Vyberte Power Platform.](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. Vyberte prostředí Power Apps, ke zkopírování a pak vyberte **Kopírovat**.

Další informace o kopírování prostředí Power Apps naleznete v části [Kopírování prostředí](/power-platform/admin/copy-environment#copy-an-environment-1).

7. Po dokončení procesu kopírování se přihlaste k cílové instanci a povolte integraci Dataverse. Další informace a pokyny naleznete v části [Konfigurace integrace Dataverse](./hr-admin-integration-common-data-service.md).

## <a name="data-elements-and-statuses"></a>Datové prvky a stavy

Při kopírování instance Human Resources nejsou zkopírovány následující datové prvky:

- E-mailové adres z tabulky **LogisticsElectronicAddress**

- Historie dávkové úlohy v tabulkách **BatchJobHistory**, **BatchHistory** a **BatchConstraintHistory**

- Heslo protokolu SMTP (Simple Mail Transfer Protocol) v tabulce **SysEmailSMTPPassword**

- Server pro předávání SMTP v tabulce **SysEmailParameters**

- Nastavení správy tisku v tabulkách **PrintMgmtSettings** a **PrintMgmtDocInstance**

- Záznamy specifické pro prostředí v tabulkách **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** a **BatchServerGroup**

- Přílohy dokumentu v tabulce DocuValue. Tyto přílohy zahrnují všechny šablony Microsoft Office, které byly přepsány ve zdrojovém prostředí.

- Připojovací řetězec v tabulce **PersonnelIntegrationConfiguration**

Některé z těchto prvků nebyly zkopírovány, protože jsou specifické pro prostředí. Příklady zahrnují záznamy **BatchServerConfig** a **SysCorpNetPrinters**. Ostatní prvky nebudou zkopírovány z důvodu objemu lístků podpory. Například:

- Mohou být odesílány duplicitní e-maily, protože v prostředí sandbox pro testování přijetí uživatele je stále povolen protokol SMTP.

- Mohou být odesílány neplatné integrační zprávy, protože dávkové úlohy jsou stále povoleny.

- Uživatelé mohou být povoleni, než mohou správci provádět akce čištění po aktualizaci.

Při kopírování instance se dále mění následující stavy:

- Všichni uživatelé s výjimkou těch, kteří mají roli zabezpečení „Správce systému“, jsou nastaveni na **Zakázáno**.

- Všechny dávkové úlohy, s výjimkou některých systémových úloh, jsou nastaveny na **srážka**.

## <a name="environment-admin"></a>Správce prostředí

Všichni uživatelé v cílovém prostředí izolovaného prostoru (sandbox) včetně správců budou nahrazeni uživateli zdrojového prostředí. Před kopírováním instance se ujistěte, zda jste správcem zdrojového prostředí. Pokud ne, nebudete se moci po dokončení kopírování přihlásit k cílovému prostředí sandbox.

Všichni uživatelé, kteří nejsou správci v cílovém prostředí izolovaného prostoru (sandbox), jsou zakázáni, aby zabránili nechtěným přihlášením v prostředí karantény. Správci mohou v případě potřeby znovu povolit uživatele.

## <a name="apply-custom-fields-to-dataverse"></a>Použití vlastních polí na Dataverse

Pokud zkopírujete instanci do prostředí sandbox a chcete integrovat prostředí sandbox s Dataverse, musíte znovu použít vlastní pole na tabulky Dataverse.

Pro každé vlastní pole, které je vystaveno v tabulkách Dataverse, proveďte následující kroky:

1. Přejděte do vlastního pole a vyberte **Upravit**.

2. Zrušte výběr pole **Povoleno** pro každou entitu cdm_*, pro kterou je povoleno vlastní pole.

3. Vyberte **Použít změny**.

4. Znovu vyberte **Upravit**.

5. Vyberte pole **Povoleno** pro každou entitu cdm_*, pro kterou je povoleno vlastní pole.

6. Znovu vyberte **Použít změny**.

Proces zrušení výběru, použití změn, opětovného výběru a opětovného použití změn vyzve schéma k aktualizaci v Dataverse pro zahrnutí vlastních polí.

Další informace o vlastních polích naleznete v tématu [Vytvoření vlastních polí a práce s nimi](../fin-ops-core/fin-ops/get-started/user-defined-fields.md).

## <a name="see-also"></a>Viz také

[Zřízení Human Resources](hr-admin-setup-provision.md)</br>
[Odebrání instance](hr-admin-setup-remove-instance.md)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
