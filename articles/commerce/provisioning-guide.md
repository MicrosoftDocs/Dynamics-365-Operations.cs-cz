---
title: Zřízení sandboxového prostředí Dynamics 365 Commerce
description: Tento článek vysvětluje, jak zřídit sandboxové prostředí Microsoft Dynamics 365 Commerce pro ukázku nebo použití sandboxu s vestavěnými ukázkovými daty.
author: josaw1
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 1fc50f98055f1df72d255a5be6e863570564b183
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283634"
---
# <a name="provision-a-dynamics-365-commerce-sandbox-environment"></a>Zřízení sandboxového prostředí Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Tento článek vysvětluje, jak zřídit sandboxové prostředí Microsoft Dynamics 365 Commerce pro ukázku použití s vestavěnými ukázkovými daty. Proces nastavení produkčního prostředí je podobný, ale propracovanější, protože mnohé z předpokladů prostředí sandbox jsou již uvedeny v demo datech.

Než začnete, doporučujeme vám tento článek rychle prohledat, abyste získali představu o tom, co proces vyžaduje.

Chcete-li úspěšně zřídit prostředí Commerce sandbox, musíte zadat některé parametry pro prostředí a Commerce Scale Unit (CSU), které budou použity při pozdějším zřízení Commerce. Pokyny v tomto článku popisují všechny požadované kroky, které je třeba provést, a parametry, které je nutné použít.

Po úspěšném zřízení prostředí Commerce je k přípravě prostředí náhledu nutné provést několik dalších kroků. Některé kroky jsou volitelné, v závislosti na aspektech systému, které chcete používat. Volitelné kroky můžete vždy dokončit později.

Informace o konfiguraci prostředí Commerce po jeho vytvoření najdete v části [konfigurace sandboxového prostředí Commerce](cpe-post-provisioning.md). Informace o konfiguraci volitelných funkcí prostředí Commerce najdete v části [konfigurace volitelných funkcí sandboxového prostředí Commerce](cpe-optional-features.md).

## <a name="prerequisites"></a>Předpoklady

Aby bylo možné zřídit prostředí Commerce, musí být zavedeny následující předpoklady:

- Máte přístup k portálu Microsoft Dynamics Lifecycle Services (LCS).
- Jste existující partner Microsoft Dynamics 365 nebo zákazník a máte již vytvořený implementační projekt a dostupný pro použití v LCS.  
- Vytvořili jste skupinu zabezpečení Azure Active Directory (Azure AD), kterou lze použít jako skupinu správců systému e-Commerce a máte k dispozici její ID.
- Vytvořili jste skupinu zabezpečení Azure AD, kterou lze použít jako skupinu pro moderátory hodnocení a recenzí a máte k dispozici její ID. (Tato skupina zabezpečení může být shodná se skupinou správců systému Commerce.)
- Nasadili jste instanci centrály v rámci LCS. Další informace viz [Nasazení nového prostředí](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).

Tento seznam není vyčerpávající. Pokud se objeví nějaké problémy, měli byste se obrátit na svého partnera společnosti Microsoft s žádostí o pomoc.

## <a name="provision-your-commerce-environment"></a>Zřizování prostředí služby Commerce

Následující postupy vysvětlují, jak zřídit prostředí Commerce. Po úspěšném dokončení těchto kroků bude prostředí Commerce připraveno na konfiguraci. Všechny níže popsané kroky se uskuteční na portálu LCS.

### <a name="initialize-the-commerce-scale-unit-cloud"></a>Inicializace Commerce Scale Unit (cloud)

Pokud chcete inicializovat CSU, postupujte takto.

1. V LCS vyberte své prostředí ze seznamu.
1. V zobrazení **PROSTŘEDÍ** napraco vyberte **Úplné podrobnosti**. Zobrazí se podrobnosti o prostředí.
1. V sekci **Spravovat prostředí** pod **VLASTNOSTI PROSTŘEDÍ** vyberte **Spravovat**.
1. Na kartě **Commerce Scale Units** vyberte **Inicializovat**. Zobrazí se pohled **Přidat jednotku škálování**.
1. V poli **OBLAST** vyberte oblast, která je stejná nebo blízká oblasti, do které jste prostředí nasadili.
1. V rozevíracím seznamu **Verze** vyberte nejnovější dostupnou verzi.
1. Vyberte **Inicializovat**.
1. V dialogovém okně varování, které vás požádá o potvrzení inicializace jednotky Commerce Scale Unit, vyberte **Ano**. Vaše CSU byla nyní zařazena do fronty pro zřizování.
1. Než budete pokračovat, ujistěte se, že je stav CSU **ÚSPĚCH**. Inicializace trvá přibližně dvě až pět hodin.

Pokud nemůžete najít odkaz **Správa** odkaz v zobrazení podrobností o prostředí, požádejte o pomoc kontaktní osobu společnosti Microsoft.

### <a name="initialize-e-commerce"></a>Inicializace e-Commerce

Pokud chcete inicializovat Commerce, postupujte takto.

1. Na kartě **Elektronické obchodování** vyberte možnost **Nastavení.**
1. V poli **Název prostředí e-Commerce** zadejte název. Uvědomte, že název bude viditelný u některých adres URL, které odkazují na vaši instanci e-Commerce.
1. V poli **Název Commerce Scale Unit** vyberte položku CSU v seznamu. (Seznam by měl mít pouze jednu možnost.)

    Pole **Geografie elektronického obchodování** je nastaveno automaticky.

1. Pokračujte výběrem tlačítka **Další**.
1. Do pole **Podporované názvyhostitelů** zadejte libovolnou platnou doménu, například `www.fabrikam.com`.
1. V poli **Skupina zabezpečení AAD pro správce systému** zadejte několik prvních písmen názvu skupiny zabezpečení, kterou chcete použít, a poté zobrazte výsledky hledání výběrem symbolu lupy. V seznamu vyberte správnou skupinu zabezpečení.
1.  V poli **Skupina zabezpečení AAD pro moderátora hodnocení a recenzování** zadejte několik prvních písmen názvu skupiny zabezpečení, kterou chcete použít, a poté zobrazte výsledky hledání výběrem symbolu lupy. V seznamu vyberte správnou skupinu zabezpečení.
1. Možnost **Povolit službu hodnocení a recenzování** nechte nastavenou na hodnotu **Ano**.
1. Vyberte **Inicializovat**. Zobrazení **Správa velkoobchodu** se objeví znovu, když je vybraná karta **e-Commerce**. Vaše inicializace e-Commerce byla zahájena.
1. Než budete pokračovat, počkejte, dokud nebude inicializační stav Commerce **INICIALIZACE ÚSPĚŠNÁ**.
1. V **Odkazech** v pravém dolním roku si poznamenejte adresy URL následujících odkazů:

    * **Web e-Commerce** – odkaz na kořenový adresář webu e-Commerce.
    * **Nástroj pro správu webu Commerce** – odkaz na nástroj pro správu webu.

## <a name="next-steps"></a>Další kroky

Chcete-li pokračovat v procesu zřizování a konfigurace prostředí Commerce, viz [Konfigurace sandboxového prostředí Commerce](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Další prostředky

[Konfigurace sandboxového prostředí Dynamics 365 Commerce](cpe-post-provisioning.md)

[Konfigurace BOPIS v sandboxovém prostředí Dynamics 365 Commerce](cpe-bopis.md)

[Konfigurace volitelných funkcí pro sandboxové prostředí Dynamics 365 Commerce](cpe-optional-features.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Commerce Scale Unit (cloud)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Portál Microsoft Azure](https://azure.microsoft.com/features/azure-portal)

[Web Dynamics 365 Commerce](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
