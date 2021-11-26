---
title: Konfigurace Finance Insights
description: Toto téma vysvětluje kroky konfigurace, které vašemu systému umožní používat funkce, které jsou k dispozici ve finančních přehledech.
author: ShivamPandey-msft
ms.date: 1/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 5668d3ddff777645b4f1c6608f025d0c5a63208a
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752971"
---
# <a name="configuration-for-finance-insights"></a>Konfigurace Finance Insights

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finanční přehledy kombinují funkčnost Microsoft Dynamics 365 Finance s Dataverse, Azure a AI Builder, které vaší organizaci poskytnou výkonné nástroje pro prognózy. Toto téma vysvětluje kroky konfigurace, které vašemu systému umožní používat funkce, které jsou k dispozici ve finančních přehledech. Chcete-li úspěšně dokončit postupy v tomto tématu, musíte mít přístup správce systému a úpravce systému v [Centru pro správu Power Portal](https://admin.powerplatform.microsoft.com/), přístup správce systému v Dynamics 365 Finance a přístup k vytváření prostředí v Microsoft Dynamics Lifecycle Services (LCS).

> [!NOTE]
> Následující postupy pro nastavení Finance Insights jsou platné pro verze Dynamics 365 Finance 10.0.21 a vyšší.

## <a name="deploy-dynamics-365-finance"></a>Nasazení Dynamics 365 Finance

Pro nasazení prostředí postupujte takto.

1. V LCS vytvořte nebo aktualizujte prostředí Dynamics 365 Finance. Prostředí vyžaduje verzi aplikace 10.0.21 nebo novější.

    > [!NOTE]
    > Prostředí musí mít vysokou dostupnost (HA) v prostředí. (Tento typ prostředí se také nazývá prostředí 2. úrovně.) Další informace najdete v tématu [Plánování prostředí](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

2. Pokud konfigurujete Finance Insights v prostředí Sandbox, možná budete muset zkopírovat produkční data do tohoto prostředí, aby předpovědi fungovaly. Predikční model využívá k sestavování předpovědí několik let dat. Demo data Contoso neobsahují dostatek historických dat pro adekvátní trénink predikčního modelu. 

## <a name="configure-dataverse"></a>Konfigurace služby Dataverse

Ke konfiguraci Dataverse pro Finance Insights proveďte následující kroky.

- Otevřete stránku prostředí v LCS a ověřte, že část **Integrace Power Platform** je již nastavena.

    - Pokud je již nastavena, název prostředí Dataverse spojený s prostředím Finance by měl být uveden.
    - Pokud ještě není nastavena, vyberte **Nastavit**. Nastavení prostředí Dataverse může trvat až hodinu. Až bude nastavení úspěšně dokončeno, název prostředí Dataverse spojený s prostředím Finance by měl být uveden.

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

## <a name="feedback-and-support"></a>Zpětná vazba a podpora

Pokud máte zájem o poskytnutí zpětné vazby nebo pokud vyžadujete technickou podporu, zašlete prosím e-mail na [Finance Insights (Preview)](mailto:fiap@microsoft.com).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
