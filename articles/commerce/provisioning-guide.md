---
title: Zřízení prostředí vyhodnocení Dynamics 365 Commerce
description: Toto téma vysvětluje, jak zřídit prostředí pro hodnocení v Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: e5ce2002c66a1c36d5647d3c76684b394fc1ff79
ms.sourcegitcommit: 5175e3fae432016246244cf70fe05465f43de88c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/17/2020
ms.locfileid: "3599843"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a>Zřízení prostředí vyhodnocení Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Toto téma vysvětluje, jak zřídit prostředí pro hodnocení v Microsoft Dynamics 365 Commerce.

Než začnete, doporučujeme vám toto téma rychle prohledat, abyste získali představu o tom, co proces vyžaduje.

> [!NOTE]
> Prostředí vyhodnocení Commerce nejsou obecně dostupná a jsou poskytována partnerům a zákazníkům na základě žádosti. Podrobnější informace získáte od kontaktu společnosti Microsoft.

## <a name="overview"></a>Přehled

Chcete-li úspěšně zřídit prostředí pro hodnocení Commerce, musíte vytvořit projekt, který má specifický název a typ produktu. Prostředí a Commerce Scale Unit (CSU) také mají některé specifické parametry, které musíte použít, když se chystáte ke zřizování e-Commerce později. Pokyny v tomto tématu popisují všechny požadované kroky, které je třeba provést, a parametry, které je nutné použít.

Po úspěšném zřízení prostředí vyhodnocení Commerce je k přípravě prostředí náhledu nutné provést několik dalších kroků. Některé kroky jsou volitelné, v závislosti na aspektech systému, které chcete vyhodnotit. Volitelné kroky můžete vždy dokončit později.

Informace o konfiguraci prostředí vyhodnocení Commerce po jeho vytvoření najdete v části [konfigurace prostředí vyhodnocení Commerce](cpe-post-provisioning.md). Informace o konfiguraci volitelných funkcí prostředí vyhodnocení Commerce najdete v části [konfigurace volitelných funkcí prostředí vyhodnocení Commerce](cpe-optional-features.md).

## <a name="prerequisites"></a>Předpoklady

Aby bylo možné zřídit prostředí vyhodnocení Commerce, musí být zavedeny následující předpoklady:

- Máte přístup k portálu Microsoft Dynamics Lifecycle Services (LCS).
- Jste stávajícím partnerem Microsoft Dynamics 365 nebo odběratelem a máte možnost vytvořit projekt Dynamics 365 Commerce.
- Máte přístup správce k vašemu předplatnému Microsoft Azure nebo jste v kontaktu se správcem předplatného, který vám může v případě potřeby pomoci.
- Máte k dispozici ID klienta Azure Active Directory (Azure AD).
- Vytvořili jste Skupinu zabezpečení Azure AD, kterou lze použít jako skupinu správců systému e-Commerce a máte k dispozici její ID.
- Vytvořili jste skupinu zabezpečení Azure AD, kterou lze použít jako skupinu pro moderátory hodnocení a recenzí a máte k dispozici její ID. (Tato skupina zabezpečení může být shodná se skupinou správců systému e-commerce.)

Tento seznam není vyčerpávající. Pokud se objeví nějaké problémy, měli byste se obrátit na svého partnera společnosti Microsoft s žádostí o pomoc.

## <a name="provision-your-commerce-evaluation-environment"></a>Zřizování prostředí vyhodnocení služby Commerce

Tyto postupy vysvětlují, jak zřídit prostředí vyhodnocení Commerce. Po úspěšném dokončení těchto nastavení bude prostředí vyhodnocení Commerce připraveno na konfiguraci. Všechny popsané aktivity se objeví na portálu LCS.

### <a name="create-a-new-project"></a>Vytvořit nový projekt

Chcete-li vytvořit nový projekt LCS pro projekt, postupujte následovně.

1. Na domovské stránce LCS vyberte znaménko plus (**+**) pro vytvoření projektu.
1. V pravém podokně proveďte jeden z následujících kroků:

    - Pokud jste partnerem, zvolte možnost **Migrovat, vytvořit řešení a získat informace**.
    - Pokud jste odběratel, vyberte možnost **Potenciální předprodeje**.

1. Zadat název a popis šablony a odvětví.
1. V poli **Název produktu** vyberte **Dynamics 365 Commerce**.
1. V poli **Verze produktu** vyberte **Dynamics 365 Commerce**.
1. V poli **Metodologie** vyberte **Metodologie implementace Dynamics Retail**.
1. Volitelné: Můžete importovat role a uživatele z existujícího projektu.
1. Vyberte **Vytvořit**. Zobrazí se projekt.

### <a name="add-the-azure-connector"></a>Přidejte konektor Azure

Chcete-li přidat Azure Connector do svého projektu LCS, postupujte podle kroků v části [Dokončení procesu integrace Azure Resource Manager (ARM)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).

### <a name="deploy-the-environment"></a>Nasazení prostředí

Pro nasazení prostředí postupujte takto.

> [!NOTE]
> Je možné, že nebudete muset dokončit kroky 6, 7 a/nebo 8, protože stránky, které mají jedinou možnost, jsou přeskočeny. V zobrazení **Parametry prostředí** potvrďte, že se text **Dynamics 365 Commerce - ukázka (10.0.* x* s aktualizací Platform *xx*)** zobrazuje přímo nad polem **Název prostředí**. Podrobnosti viz obrázek, který se zobrazí po kroku 8.

1. V horní nabídce vyberte možnost **Prostředí hostovaná v cloudu**.
1. Prostředí přidáte výběrem tlačítka **Přidat**.
1. V poli **verze aplikace** vyberte nejaktuálnější verzi. Pokud máte specifickou potřebu vybrat jinou než nejaktuálnější verzi aplikace, nevybírejte verzi před **10.0.8**.
1. V poli **verze platformy** použijte verzi platformy, která je automaticky vybrána pro vybranou verzi aplikace. 

    ![Vyběr verze aplikace a platformy](./media/project1.png)

1. Zvolte **Další**.
1. Výberte **Demo** jako topologii prostředí.

    ![Výběr topologie prostředí 1](./media/project2.png)

1. Na stránce **Nasadit prostředí** zadejte název prostředí. Ponechte Upřesňující nastavení, jak je.

    ![Stránka Nasazení prostředí](./media/project4.png)

1. Upravte velikost VM podle potřeby. (Doporučujeme skladovou jednotku VM \[SKU\] **D13 v2**.)
1. Zkontrolujte ceny a licenční podmínky a pak zaškrtnutím políčka označte, že s nimi souhlasíte.
1. Zvolte **Další**.
1. Na stráncee s potvrzením nasazení ověřte správnost podrobností klikněte vyberte **Nasadit**. Vrátíte se do zobrazení **Prostředí hostovaná v cloudu** a v seznamu se zobrazí vaše prostředí.

    Požadované prostředí bude zobrazeno jako zařazeno do fronty a potom nasazeno. Dokončení pracovních postupů prostředí bude trvat určitou dobu. Proto se vraťte přibližně za 6 až 9 hodin.

1. Než budete pokračovat, ujistěte se, že je stav prostředí **Nasazený**.

### <a name="initialize-the-commerce-scale-unit-cloud"></a>Inicializace Commerce Scale Unit (cloud)

Pokud chcete inicializovat CSU, postupujte takto.

1. V zobrazení **Prostředí hostovaná v cloudu** vyberte v seznamu požadované prostředí.
1. V zobrazení prostředí napraco vyberte **úplné podrobnosti**. Zobrazí se podrobnosti o prostředí.
1. V části **Funkce prostředí** vyberte **Spravovat**.
1. Na kartě **Velkoobchod** vyberte **Inicializovat**. Zobrazí se zobrazení inicializačních parametrů CSU.
1. V poli **Oblast** vyberte oblast, která je stejná nebo blízká oblasti, do které jste prostředí nasadili.
1. Nechte pole **Verze** tak, jak je.
1. Vyberte **Inicializovat**.
1. Na stráncee s potvrzením nasazení ověřte správnost podrobností klikněte vyberte **Ano**. Zobrazení **Správa velkoobchodu** se objeví znovu, když je vybraná karta **Commerce**. Vaše CSU byla zařazena do fronty pro zřizování.
1. Než budete pokračovat, ujistěte se, že je stav CSU **Úspěch**. Inicializace trvá přibližně dvě až pět hodin.

Pokud nemůžete najít odkaz **Správa** odkaz v zobrazení podrobností o prostředí, požádejte o pomoc kontaktní osobu společnosti Microsoft.

### <a name="initialize-e-commerce"></a>Inicializace e-Commerce

Pokud chcete inicializovat e-Commerce, postupujte takto.

1. Na kartě **e-Commerce** zkontrolujte souhlas s vyhodnocením a pak vyberte **Nastavení**.
1. V poli **Název prostředí e-Commerce** zadejte název. Uvědomte, že název bude viditelný u některých adres URL, které odkazují na vaši instanci e-Commerce.
1. V poli **Název Commerce Scale Unit** vyberte položku CSU v seznamu. (Seznam by měl mít pouze jednu možnost.)

    Pole **Geografie elektronického obchodování** je nastaveno automaticky.

1. Pokračujte výběrem tlačítka **Další**.
1. Do pole **Podporované názvyhostitelů** zadejte libovolnou platnou doménu, například `www.fabrikam.com`.
1. V poli **Skupina zabezpečení AAD pro správce systému** zadejte několik prvních písmen názvu skupiny zabezpečení, kterou chcete použít, a poté zobrazte výsledky hledání výběrem symbolu lupy. V seznamu vyberte správnou skupinu zabezpečení.
1.  V poli **Skupina zabezpečení AAD pro moderátora hodnocení a recenzování** zadejte několik prvních písmen názvu skupiny zabezpečení, kterou chcete použít, a poté zobrazte výsledky hledání výběrem symbolu lupy. V seznamu vyberte správnou skupinu zabezpečení.
1. Možnost **Povolit službu hodnocení a recenzování** nechte nastavenou na hodnotu **Ano**.
1. Vyberte **Inicializovat**. Zobrazení **Správa velkoobchodu** se objeví znovu, když je vybraná karta **e-Commerce**. Vaše inicializace e-Commerce byla zahájena.
1. Než budete pokračovat, počkejte, dokud nebude inicializační stav e-Commerce **Inicializace úspěšná**.
1. V **Odkazech** v pravém dolním roku si poznamenejte adresy URL následujících odkazů:

    * **Web e-Commerce** – odkaz na kořenový adresář webu e-Commerce.
    * **Nástroj pro správu webu Commerce** – odkaz na nástroj pro správu webu.

## <a name="next-steps"></a>Další kroky

Chcete-li pokračovat v procesu zřizování a konfigurace prostředí vyhodnocení Commerce, přečtěte si část [Konfigurace prostředí pro náhled Commerce](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Další prostředky

[Přehled prostředí vyhodnocení Dynamics 365 Commerce](cpe-overview.md)

[Konfigurace prostředí vyhodnocení Dynamics 365 Commerce](cpe-post-provisioning.md)

[Konfigurovat BOPIS v prostředí vyhodnocení Dynamics 365 Commerce](cpe-bopis.md)

[Konfigurace volitelných funkcí pro prostředí vyhodnocení aplikace Dynamics 365 Commerce](cpe-optional-features.md)

[Časté otázky týkající se prostředí vyhodnocení Dynamics 365 Commerce](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Commerce Scale Unit (cloud)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Portál Microsoft Azure](https://azure.microsoft.com/features/azure-portal)

[Web Dynamics 365 Commerce](https://aka.ms/Dynamics365CommerceWebsite)
