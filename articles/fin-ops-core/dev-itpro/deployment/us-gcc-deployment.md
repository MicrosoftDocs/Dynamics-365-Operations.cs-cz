---
title: Dynamics 365 Finance, Supply Chain Management a Commerce v US Government Community Cloud (GCC)
description: Toto téma poskytuje informace o produktech Microsoft Dynamics 365 US Government, které jsou k dispozici kvalifikovaným státním a soukromým entitám.
author: hasaid
ms.date: 11/12/2021
ms.topic: article
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2021-11-09
ms.openlocfilehash: 204bf1886ff7f7393fba5713a54f305274f540d0
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693301"
---
# <a name="dynamics-365-finance-supply-chain-management-and-commerce-in-us-government-community-cloud-gcc"></a>Dynamics 365 Finance, Supply Chain Management a Commerce v US Government Community Cloud (GCC)

[!include [banner](../includes/banner.md)]



Vyberte produkty United States (US) Government Microsoft Dynamics 365, které jsou k dispozici kvalifikovaným státním a soukromým entitám. Tyto entity jsou omezeny na následující typy:

- Federální, státní, místní, kmenové a teritoriální vládní entity USA
- Soukromé subjekty, které používají Dynamics 365 US Government k poskytování řešení vládním subjektům nebo kvalifikovaným členům cloudové komunity
- Soukromé subjekty, které mají zákaznická data, která podléhají vládním nařízením, a Dynamics 365 US Government je vhodnou službou pro splnění regulačních požadavků.

Další informace viz [Dynamics 365 US Government](/power-platform/admin/microsoft-dynamics-365-government).

## <a name="onboarding"></a>Nábor

Pro dokončení úvodního onboardingu pro implementační projekt v Microsoft Dynamics Lifecycle Services (LCS) postupujte podle pokynů v tématu [Nasadit implementační projekt](../../../fin-ops-core/fin-ops/imp-lifecycle/onboard.md). Nepoužívejte však odkaz na veřejné LCS, který je uveden v těchto pokynech. Místo toho použijte následující adresu URL k otevření LCS pro US Government Community Cloud (GCC): <https://gov.lcs.microsoftdynamics.us>.

Po dokončení počátečního onboardingu postupujte podle pokynů v [Onboardingu projektu](../lifecycle-services/project-onboarding.md). Ještě jednou použijte [LCS pro GCC](https://gov.lcs.microsoftdynamics.us) místo veřejného LCS.

## <a name="environment-deployment"></a>Nasazení prostředí

Po dokončení onboardingu projektu si můžete prohlédnout další možnosti LCS, které jsou popsány v [Lifecycle Services (LCS) pro zákazníky finančních a provozních aplikací](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md). Poté přejděte k nasazení prostředí.

- Chcete-li nasadit prostředí spravovaná společností Microsoft prostřednictvím LCS, postupujte podle pokynů v [Lifecycle Services (LCS) pro zákazníky finančních a provozních aplikací](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md#new-deployment-experience).
- Pro prostředí hostovaná v cloudu viz [Nasazení a přístup k vývojovým prostředím](../../../fin-ops-core/dev-itpro/dev-tools/access-instances.md). Musíte také dokončit proces onboardingu rámce Resource Manager pro vaše konektory, jak je popsáno v [Dokončit proces onboardingu Azure Resource Manager pro projekty US government Lifecycle Services](arm-onbarding-us-goverment.md).

> [!NOTE]
> U projektů LCS US Government jsou podporována pouze předplatná Azure specifická pro Azure Government.

## <a name="features-that-arent-available"></a>Funkce, které nejsou k dispozici

Některé funkce nebudou k dispozici pro nasazení v GCC nebo nebudou k dispozici pro použití s Dynamics 365 v GCC. Například, služby Azure DevOps nebudou v GCC dostupné. Nicméně lze využít místní Azure DevOps nebo veřejné služby Azure DevOps. Podrobné informace o dostupnosti funkcí viz [Dostupnost funkcí Business Applications US Government](https://aka.ms/BAPFunctionalParity).

## <a name="frequently-asked-questions"></a>Časté dotazy

### <a name="are-dynamics-365-finance-and-dynamics-365-supply-chain-management-supported-in-gcc-high"></a>Jsou Dynamics 365 Finance a Dynamics 365 Supply Chain Management podporovány v GCC-High?

Číslo Dynamics 365 Finance a Dynamics 365 Supply Chain Management podporovány pouze v GCC.

### <a name="can-i-use-public-azure-devops-with-finance-and-supply-chain-management-in-gcc"></a>Mohu použít veřejné Azure DevOps s Finance a Supply Chain Management v GCC?

Ano, můžete použít veřejné služby Azure DevOps, pokud nemáte požadavky na řešení, které je certifikováno programem Federal Risk and Authorization Management Program (FEDRAMP). Případně můžete použít Azure DevOps server.

### <a name="can-i-deploy-a-cloud-hosted-environment-tier-1-development-environment-on-an-azure-commercial-subscription"></a>Mohu nasadit vývojové prostředí úrovně 1 hostovaného v cloudu v předplatném Azure Commercial?

Č. V [LCS pro GCC](https://gov.lcs.microsoftdynamics.us) musíte k nasazení prostředí hostovaného v cloudu použít předplatné Azure Government.

### <a name="what-can-i-do-if-i-need-a-package-from-the-shared-asset-library-but-it-isnt-available-in-lcs-for-gcc"></a>Co mohu udělat, když potřebuji balíček z knihovny sdíleného majetku, ale není dostupný v LCS pro GCC?

Stejný balíček si můžete stáhnout z knihovny sdíleného majetku ve [veřejných LCS](https://lcs.dynamics.com). Případně vám může váš partner pomoci balíček stáhnout.

### <a name="is-the-code-upgrade-tool-available-in-gcc"></a>Je nástroj pro upgrade kódu dostupný v GCC?

Ne, nástroj pro upgrade kódu není aktuálně v GCC k dispozici. Můžete však vytvořit potenciální projekt ve [veřejných LCS](https://lcs.dynamics.com) a použít nástroj pro upgrade kódu. Všimněte si, že nebudete moci nasadit prostředí v potenciálních projektech.

### <a name="can-my-partner-open-a-support-ticket-on-my-behalf"></a>Může můj partner otevřít lístek podpory mým jménem?

Ano. Pokud však váš partner používá identitu mimo GCC, lístek podpory bude přesměrován do veřejné fronty podpory. Doporučujeme, abyste k otevření lístků podpory použili oprávnění zákazníka GCC v LCS.

## <a name="see-also"></a>Viz také

- [Dynamics 365 US Government](/power-platform/admin/microsoft-dynamics-365-government)
- [Dostupnost funkcí Business Applications US Government](https://aka.ms/BAPFunctionalParity).
- [Uživatelská příručka Lifecycle Services (LCS)](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [Přehled cloudového nasazení](../../../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
