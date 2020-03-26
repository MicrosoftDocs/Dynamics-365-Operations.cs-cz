---
title: Kopírovat instanci
description: Pomocí služby Microsoft Dynamics Lifecycle Services (LCS) můžete kopírovat databázi Microsoft Dynamics 365 Human Resources do prostředí izolovaného prostoru (sandbox).
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bb363369994d99f358be0c23cdaf1dbc80b644e5
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092285"
---
# <a name="copy-an-instance"></a>Kopírovat instanci

Pomocí služby Microsoft Dynamics Lifecycle Services (LCS) můžete kopírovat databázi Microsoft Dynamics 365 Human Resources do prostředí izolovaného prostoru (sandbox). Máte-li jiné prostředí izolovaného prostoru (sandbox), můžete také zkopírovat databázi z prostředí do cíleného prostředí sandbox.

Chcete-li zkopírovat instanci, je nutné zajistit následující:

- Instance aplikace Human Resources, kterou chcete přepsat, musí být prostředí izolovaného prostoru (sandbox).

- Prostředí, ze kterých kopírujete, musí být ve stejné oblasti. Nelze kopírovat mezi oblastmi.

- Musíte být správcem cílového prostředí, abyste se k němu mohli po zkopírování instance přihlásit.

- Při kopírování databáze aplikace Human Resources nejsou zkopírovány prvky (aplikace nebo data), které jsou obsaženy v prostředí Microsoft PowerApps. Informace o tom, jak kopírovat prvky do prostředí PowerApps, naleznete v tématu [kopírování prostředí](https://docs.microsoft.com/power-platform/admin/copy-environment). Prostředí PowerApps, které chcete přepsat, musí být prostředí izolovaného prostoru (sandbox). Chcete-li změnit produkční prostředí PowerApps na prostředí s izolovaným prostorem, musíte být globálním správcem klienta. Další informace o změně prostředí PowerApps naleznete v tématu [přepnutí instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).

## <a name="effects-of-copying-a-human-resources-database"></a>Vliv kopírování databáze aplikace Human Resources

Při kopírování databáze aplikace Human Resources dojde k následujícím událostem:

- Při kopírování bude existující databáze vymazána v cílovém prostředí. Po dokončení kopírování nelze stávající databázi obnovit.

- Cílové prostředí nebude k dispozici, dokud nebude proces kopírování dokončen.

- Dokumenty v úložišti objektů BLOB Microsoft Azure nejsou kopírovány z jednoho prostředí do jiného. Proto nebudou žádné připojené dokumenty a šablony, které jsou připojeny, zkopírovány a zůstanou ve zdrojovém prostředí.

- Všichni uživatelé, kromě správce a ostatních interních uživatelských účtů služby budou nedostupní. Správce tedy může odstranit nebo zamlžit data před tím, než se budou moci ostatní uživatelé vrátit do systému.

- Uživatel s oprávněními správce musí provést požadované změny konfigurace, například opětovné připojení koncových bodů integrace pro určité služby nebo adresy URL.

## <a name="copy-the-human-resources-database"></a>Kopírování databáze aplikace Human Resources

Chcete-li dokončit tento úkol, nejprve zkopírujte instanci a poté se přihlaste do centra pro správu Microsoft Power Platform a zkopírujte vaše prostředí PowerApps.

> [!WARNING]
> Při kopírování instance je databáze vymazána v cílové instanci. Cílová instance není během tohoto procesu k dispozici.

1. Přihlaste se k LCS a vyberte projekt LCS obsahující instanci, kterou chcete zkopírovat.

2. Ve svém LCS projektu vyberte dlaždici **Správa aplikace Human Resources**.

3. Vyberte instanci, kterou chcete zkopírovat, a pak vyberte **Kopírovat**.

4. V podokně úloh **Kopírovat instanci** vyberte instanci, kterou chcete přepsat, a poté vyberte možnost **kopírovat**. Počkejte, až bude hodnota pole **Kopírovat stav** aktualizována na hodnotu **dokončeno**.

   ![[Výběr instance, kterou chcete přepsat](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. Vyberte **Power Platform** a přihlaste se do centra pro správu Microsoft Power Platform.

   ![[Výběr Power Platform](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. Vyberte prostředí PowerApps, ke zkopírování a pak vyberte **Kopírovat**.

7. Po dokončení procesu kopírování se přihlaste k cílové instanci a povolte integraci Common Data Service. Další informace a pokyny naleznete v části [Konfigurace integrace Common Data Service](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).

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

Některé z těchto prvků nebyly zkopírovány, protože jsou specifické pro prostředí. Příklady zahrnují záznamy **BatchServerConfig** a **SysCorpNetPrinters**. Ostatní prvky nebudou zkopírovány z důvodu objemu lístků podpory. Je například možné, že duplicitní e-maily budou odeslány, protože v prostředí pro testování přijetí uživatele (sandbox) je stále povolen protokol SMTP, mohou být odeslány neplatné integrační zprávy, protože jsou stále povoleny dávkové úlohy a uživatelé mohou být povoleni předtím, než mohou správci provést akce čištění po aktualizaci.

Při kopírování instance se dále mění následující stavy:

- Všichni uživatelé s výjimkou správce jsou nastaveni na **Zakázáno**.

- Všechny dávkové úlohy, s výjimkou některých systémových úloh, jsou nastaveny na **srážka**.

## <a name="environment-admin"></a>Správce prostředí

Všichni uživatelé v cílovém prostředí izolovaného prostoru (sandbox) včetně správců budou nahrazeni uživateli zdrojového prostředí. Před kopírováním instance se ujistěte, zda jste správcem cílového prostředí. Pokud ne, nebudete se moci po dokončení kopírování přihlásit k cílovému prostředí izolovaného prostoru (sandbox).

Všichni uživatelé, kteří nejsou správci v cílovém prostředí izolovaného prostoru (sandbox), jsou zakázáni, aby zabránili nechtěným přihlášením v prostředí karantény. Správci mohou v případě potřeby znovu povolit uživatele.
