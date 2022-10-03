---
title: Konfigurace Finance Insights
description: Tento článek vysvětluje kroky konfigurace, které vašemu systému umožní používat funkce, které jsou k dispozici ve finančních přehledech.
author: ShivamPandey-msft
ms.date: 09/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 05bf5fe5a5ff86bbf52ed58ee6b1e84c15bf2c1e
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573170"
---
# <a name="configuration-for-finance-insights"></a>Konfigurace Finance Insights

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finance Insights kombinují funkčnost Microsoft Microsoft Dynamics 365 Finance s Dataverse, Azure a AI Builder, které vaší organizaci poskytnou výkonné nástroje pro prognózy. Tento článek vysvětluje kroky konfigurace, které vašemu systému umožní používat funkce, které jsou k dispozici ve finančních přehledech. Chcete-li úspěšně dokončit postupy v tomto článku, musíte mít přístup správce systému a úpravce systému v [Centru pro správu Power Portal](https://admin.powerplatform.microsoft.com/), přístup správce systému v Dynamics 365 Finance a přístup k vytváření prostředí v Microsoft Dynamics Lifecycle Services (LCS).

> [!NOTE]
> Následující postupy pro nastavení Finance Insights jsou platné pro verze Dynamics 365 Finance 10.0.21 a vyšší.

## <a name="deploy-dynamics-365-finance"></a>Nasazení Dynamics 365 Finance

Pro nasazení prostředí postupujte takto.

1. V LCS vytvořte nebo aktualizujte prostředí Dynamics 365 Finance. Prostředí vyžaduje verzi aplikace 10.0.21 nebo novější.

    > [!NOTE]
    > Prostředí musí mít vysokou dostupnost (HA) v prostředí. (Tento typ prostředí se také nazývá prostředí 2. úrovně.) Další informace najdete v tématu [Plánování prostředí](/fin-ops-core/fin-ops/imp-lifecycle/environment-planning).

2. Pokud konfigurujete Finance Insights v prostředí Sandbox, možná budete muset zkopírovat produkční data do tohoto prostředí, aby předpovědi fungovaly. Predikční model využívá k sestavování předpovědí několik let dat. Demo data Contoso neobsahují dostatek historických dat pro adekvátní trénink predikčního modelu. 

## <a name="configure-your-azure-ad-tenant"></a>Konfigurujte svého klienta Azure AD

Azure Active Directory (Azure AD) musí být nakonfigurován tak, aby jej bylo možné používat s Dataverse a aplikacemi Microsoft Power Platform. Tato konfigurace vyžaduje buď roli **Vlastník projektu** nebo **Manažer prostředí** přiřazenou uživateli v poli **Role zabezpečení projektu** v LCS.

Ověřte, že je dokončeno následující nastavení:

- Máte přístup **Správce systému** a **Kustomizer systému** v centru pro správu Power Portal.
- Licence Dynamics 365 Finance nebo ekvivalentní licence je použita na uživatele, který instaluje doplněk Finance insights.
- Následující aplikace Azure AD jsou registrovány v Azure AD.

    |  Aplikace                             | ID aplikace                               |
    |------------------------------------------|--------------------------------------|
    | Mikroslužby CDS Microsoft Dynamics ERP | 703e2651-d3fc-48f5-942c-74274233dba8 |

    Chcete-li ověřit, zda je aplikace registrována v Azure AD, zkontrolujte seznam **Všechny aplikace**. Další podrobnosti viz [Zobrazení podnikových aplikací](/azure/active-directory/manage-apps/view-applications-portal).
  
    Pokud není aplikace registrována v Azure AD, kontaktujte podporu.
  
## <a name="configure-dataverse"></a>Konfigurace služby Dataverse

Ke konfiguraci Dataverse pro Finance Insights proveďte následující kroky.

- Otevřete stránku prostředí v LCS a ověřte, že část **Integrace Power Platform** je již nastavena.

    - Pokud je již nastaven Dataverse, název prostředí Dataverse spojený s prostředím Finance by měl být uveden.
    - Pokud Dataverse ještě není nastaven, vyberte **Nastavit**. Nastavení prostředí Dataverse může trvat až hodinu. Až bude nastavení úspěšně dokončeno, název prostředí Dataverse spojený s prostředím Finance by měl být uveden.
    - Pokud byla tato integrace nastavena s existujícím prostředím Microsoft Power Platform, obraťte se na svého správce, aby se ujistil, že propojené prostředí není v deaktivovaném stavu.

        Další informace naleznete v tématu [Povolení integrace Power Platform](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md). 

        Pro přístup k webu správce Microsoft Power Platform přejděte na <https://admin.powerplatform.microsoft.com/environments>.

## <a name="configure-the-finance-insights-add-in"></a>Konfigurace doplňku Finance Insights

Pokud jste si dříve nainstalovali doplněk Finance Insights, odinstalujte jej před dokončením následujícího postupu.

> [!NOTE]
> Pokud jste si již nainstalovali doplněk Data Lake do LCS, Finance Insights jej použijí k uložení dat, která jsou nezbytná pro předpovědi. Pokud jste ještě nenainstalovali doplněk datové jezero v LCS, doplněk Finance Insights vám vytvoří spravované datové jezero.

Podle těchto pokynů nainstalujte doplněk Finance Insights.

1. Přihlaste se do LCS a poté pod názvem prostředí na pravé straně stránky vyberte **Úplné podrobnosti**.
2. V sekci **Doplňky prostředí** vyberte **Nainstalovat nový doplněk**.
3. Vyberte doplněk **Finance Insights**.
4. Vyjárřete souhlas se smluvními podmínkami a poté vyberte možnost **Instalovat**.

Instalace doplňku může trvat několik minut.

## <a name="one-last-thing"></a>Poslední věc...

Po úspěšné instalaci doplňku může trvat až hodinu, než budete moci aktivovat funkce Finance Insights v pracovním prostoru **Správa funkcí** v Dynamics 365 Finance. Pokud nechcete čekat tak dlouho, můžete spustit ručně proces **Kontrola stavu poskytování statistik**. 

1. V Dynamics 365 Finance přejděte na **Správa systému \> Nastavení \> Automatizace procesů**.
2. Na kartě **Procesy na pozadí** najděte **Kontrola stavu poskytování přehledů** a vyberte **Upravit**.
3. Nastavte pole **Další spuštění** pole na 30 minut před aktuálním časem.

   Tato změna by měla vynutit, aby se proces **Kontrola stavu poskytování přehledů** spustil okamžitě.

   Po úspěšném dokončení procesu **Kontrola stavu poskytování přehledů** můžete povolit funkce Finance Insights v pracovním prostoru **Správa funkcí**.

> [!NOTE]
> Pokud se proces **Kontrola stavu poskytování statistik** nespustí, přejděte do **Správa systému** > **Dotazy** > **Dávkové úlohy**. V poli **Systém dotazování automatizace procesu** změňte hodnotu na **Čekání** k zahájení procesu. 
> 
## <a name="feedback-and-support"></a>Zpětná vazba a podpora

Pokud máte zájem o poskytnutí zpětné vazby nebo pokud vyžadujete technickou podporu, zašlete prosím e-mail na [Finance Insights (Preview)](mailto:fiap@microsoft.com).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
