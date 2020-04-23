---
title: Zřízení prostředí Preview aplikace Dynamics 365 Commerce
description: Toto téma vysvětluje, jak zřídit ukázkové prostředí v Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/10/2020
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
ms.openlocfilehash: d54db89372a0f9ef5b267d25e14067e3243a803c
ms.sourcegitcommit: 4254acb3cf8c6299fc2f3818ea6c499f058320d9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/09/2020
ms.locfileid: "3254741"
---
# <a name="provision-a-dynamics-365-commerce-preview-environment"></a>Zřízení prostředí Preview aplikace Dynamics 365 Commerce


[!include [banner](includes/banner.md)]

Toto téma vysvětluje, jak zřídit ukázkové prostředí v Dynamics 365 Commerce.

Než začnete, doporučujeme vám toto téma rychle prohledat, abyste získali představu o tom, co proces vyžaduje.

> [!NOTE]
> Pokud ještě nemáte přístup k Dynamics 365 Commerce Preview, můžete si vyžádat přístup k náhledu z webu [Dynamics 365 Commerce](https://aka.ms/Dynamics365CommerceWebsite).

## <a name="overview"></a>Přehled

Chcete-li úspěšně zřídit prostředí pro náhled Commerce, musíte vytvořit projekt, který má specifický název a typ produktu. Prostředí a commerce scale unit (CSU) také mají některé specifické parametry, které musíte použít ke zřizování e-Commerce později. Pokyny v tomto tématu popisují všechny požadované kroky, které je třeba provést, a parametry, které je nutné použít.

Po úspěšném zřízení ukázkového prostředí Commerce je k přípravě prostředí náhledu nutné provést několik dalších kroků. Některé kroky jsou volitelné, v závislosti na aspektech systému, které chcete vyhodnotit. Volitelné kroky můžete vždy dokončit později.

Informace o konfiguraci prostředí pro náhled Commerce po jeho vytvoření najdete v části [konfigurace prostředí pro náhled Commerce](cpe-post-provisioning.md). Informace o konfiguraci volitelných funkcí prostředí pro náhled Commerce najdete v části [konfigurace volitelných funkcí prostředí pro náhled Commerce](cpe-optional-features.md).

Pokud máte dotazy týkající se kroků zřizování nebo pokud se vyskytnou nějaké problémy, sdělte je společnosti Microsoft na [Microsoft Dynamics 365 Commerce, skupina náhledu Yammer](https://aka.ms/Dynamics365CommercePreviewYammer).

## <a name="prerequisites"></a>Předpoklady

Aby bylo možné zřídit prostředí pro náhled Commerce, musí být zavedeny následující předpoklady:

- Máte přístup k portálu Microsoft Dynamics Lifecycle Services (LCS).
- Jste stávajícím partnerem Microsoft Dynamics 365 nebo odběratelem a máte možnost vytvořit projekt Dynamics 365 Commerce.
- Byli jste přijati do programu náhledu Dynamics 365 Commerce.
- Máte požadovaná oprávnění k vytvoření projektu pro **migraci, vytvoření řešení a další informace**.
- Máte roli **Správce prostředí** nebo **Vlastník projektu** v projektu, kde se chystáte zřídit prostředí.
- Máte přístup pro správu ke svému předplatnému Microsoft Azure nebo jste v kontaktu se správcem předplatného, který může provést dva kroky, které pro vás vyžadují oprávnění správce.
- Máte k dispozici ID klienta Azure Active Directory (Azure AD).
- Vytvořili jste Skupinu zabezpečení Azure AD, kterou lze použít jako skupinu správců systému e-Commerce a máte k dispozici její ID.
- Vytvořili jste skupinu zabezpečení Azure AD, kterou lze použít jako skupinu pro moderátory hodnocení a recenzí a máte k dispozici její ID. (Tato skupina zabezpečení může být shodná se skupinou správců systému e-commerce.)

## <a name="provision-your-commerce-preview-environment"></a>Zřizování ukázkového prostředí služby Commerce

Tyto postupy vysvětlují, jak zřídit prostředí pro náhled Commerce. Po úspěšném dokončení těchto nastavení bude prostředí pro náhled Commerce připraveno na konfiguraci. Všechny popsané aktivity se objeví na portálu LCS.

> [!IMPORTANT]
> Přístup k náhledu je svázán s účtem LCS a organizací, kterou jste určili v aplikaci Commerce pro náhled. K zajištění prostředí náhledu Commerce je nutné použít stejný účet. Pokud potřebujete použít jiný účet LCS nebo nájemce pro prostředí náhledu Commerce, musíte tyto podrobnosti poskytnout společnosti Microsoft. Kontaktní informace naleznete v části [Podpora ukázkového prostředí Commerce](#commerce-preview-environment-support) dále v tomto tématu.

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a>Zkontrolujte, zda jsou k dispozici funkce náhledu a zda jsou zapnuty v LCS.

Chcete-li zkontrolovat, zda jsou k dispozici funkce náhledu a zda jsou zapnuty v LCS, postupujte náledovně.

1. Přihlaste se k [portálu LCS](https://lcs.dynamics.com) pomocí stejného účtu LCS, který jste použili k vyžádání přístupu k náhledu.
1. Na domovské stránce LCS posuňte se úplně doprava a vyberte dlaždici **Správa funkcí náhledu**.

    ![Dlaždice správy verze Preview](./media/preview1.png)

1. Posuňte se dolů k **Funkcím soukromého náhledu** a zkontrolujte, zda jsou dostupné a zapnuté následující funkce:

    - Hodnocení e-Commerce
    - Prostředí služby Commerce Preview

    ![Funkce soukromé verze Preview](./media/preview2.png)

1. Pokud se tyto funkce v seznamu neobjeví, obraťte se na společnost Microsoft a poskytněte své pracovní e-mailové adresy, účet LCS a podrobnosti o klientovi. Kontaktní informace naleznete v části [Podpora ukázkového prostředí Commerce](#commerce-preview-environment-support).

### <a name="create-a-new-project"></a>Vytvořit nový projekt

Chcete-li vytvořit nový projekt LCS pro projekt, postupujte následovně.

1. Na domovské stránce LCS vyberte znaménko plus (**+**) pro vytvoření projektu.
1. V pravém podokně proveďte jeden z následujících kroků:

    - Pokud jste partnerem, zvolte možnost **Migrovat, vytvořit řešení a získat informace**.
    - Pokud jste odběratel, vyberte možnost **Potenciální předprodeje**.

1. Zadat název a popis šablony a odvětví.
1. V poli **Název produktu** vyberte **Dynamics 365 Retail**.
1. V poli **Verze produktu** vyberte **Dynamics 365 Retail**.
1. V poli **Metodologie** vyberte **Metodologie implementace Dynamics Retail**.
1. Volitelné: Můžete importovat role a uživatele z existujícího projektu.
1. Vyberte **Vytvořit**. Zobrazí se projekt.

### <a name="add-the-azure-connector"></a>Přidejte konektor Azure

Chcete-li přidat Azure konektor do projektu LCS, postupujte následovně.

1. Proveďte jeden z následujících kroků:

    - Pokud jste partnerem, vyberte dlaždici **Nastavení projektu** zcela vpravo.
    - Pokud jste odběratel, zvolte **Nastavení projektu** z horní nabídky.

1. Vyberte **Konektory Azure**.
1. Chcete-li přidat konektor Azure, klikněte na tlačítko **Přidat**.
1. Zadejte název.
1. Vložte své ID předplatného Azure.
1. Zapněte možnost **Konfigurovat pro použití technologie ARM (Azure Resource Manager)**.
1. Ověřte správnost hodnoty **Domény klienta předplatného služby Azure AAD ( nebo ID)**. V případě potřeby se obraťte na správce předplatného Azure.
1. Zvolte **Další**.
1. Podle pokynů na stránce udělte požadovaným aplikacím přístup k vašemu předplatnému. V případě potřeby se obraťte na správce předplatného Azure.

    1. Přihlaste se do [portálu Azure](https://portal.azure.com/).
    1. Přesvědčte se, zda je vybrán správný adresář, a v levé nabídce vyberte položku **odběry**.
    1. Vyhledejte správné předplatné ze seznamu a vyberte je. Podle potřeby použijte funkci vyhledávání.
    1. V nabídce vyberte příkaz **Řízení přístupu (IAM)**.
    1. Napravo v sekci **Přidat přiřazení rolí** vyberte **Přidat**. Objeví se podokno **Přidat přiřazení role**.
    1. V poli **Role** vyberte **Přispěvatel**.
    1. V poli **Přiřadit přístup k** ponechejte výchozí hodnotu, uživatele **Azure AD, skupinu nebo hlavní název služby**.
    1. V možnosti **Vybrat** vložte **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.
    1. Vyberte **Služba pro nasazení aplikace Dynamics \[wsfed-enabled\]** ze seznamu.
    1. Zvolte **Uložit**.

1. Zvolte **Další**.
1. Podle pokynů na stránce udělte požadovaným aplikacím přístup k vašemu předplatnému. V případě potřeby se obraťte na správce předplatného Azure.
1. Zvolte **Další**.
1. V poli **Oblast Azure** zvolte **East US**, **East US 2**, **West US** nebo **West US 2**.
1. Vyberte **Připojit**. V seznamu by se měl zobrazit konektor Azure.

### <a name="import-the-commerce-preview-demo-base-extension"></a>Importovat Náhled rozšíření ukázky Commerce

Chcete-li importovat Náhled rozšíření ukázky Commerce do projektu, postupujte následovně.

1. Otevřete domovskou stránku projektu výběrem názvu projektu v horní části.
1. Proveďte jeden z následujících kroků:

    - Pokud jste partnerem, vyberte dlaždici **Knihovna prostředků** zcela vpravo.
    - Pokud jste odběratel, zvolte **Knihovna prostředků** z horní nabídky.

1. Ze seznamu vlevo vyberte **Balíček nasazení softwaru**.
1. Vyberte **Import**.
1. V **Knihovně sdílených prostředků** vyberte **Náhled rozšíření ukázky Commerce** v knihovně prostřeků.
1. Vyberte **Zvolit**. Vrátíte se do knihovny majetku a toto rozšíření se zobrazí v seznamu.

Následující ilustrace znázorňuje akce, které je třeba provést na stránce **Knhovna prostředků** LCS.

![Import Náhled rozšíření ukázky Commerce](./media/import.png)

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

1. Jako topologii prostředí vyberte **Dynamics 365 Commerce - ukázka**. Pokud jste dříve nakonfigurovali jeden konektor Azure Connector, bude se používat pro toto prostředí. Pokud jste nakonfigurovali více konektorů Azure, můžete vybrat, kterou spojnici chcete použít: **:Východ USA**, **Východ USA 2**, **Západ USA** nebo **Západ USA 2**. (Pro dosažení nejlepšího výkonu doporučujeme vybrat **Západ USA 2**.)

    ![Výběr topologie prostředí 2](./media/project3.png)

1. Na stránce **Nasadit prostředí** zadejte název prostředí. Ponechte Upřesňující nastavení, jak je.

    ![Stránka Nasazení prostředí](./media/project4.png)

1. Upravte velikost VM podle potřeby. (Doporučujeme skladovou jednotku VM \[SKU\] **D13 v2**.)
1. Zkontrolujte ceny a licenční podmínky a pak zaškrtnutím políčka označte, že s nimi souhlasíte.
1. Zvolte **Další**.
1. Na stráncee s potvrzením nasazení ověřte správnost podrobností klikněte vyberte **Nasadit**. Vrátíte se do zobrazení **Prostředí hostovaná v cloudu** a v seznamu se zobrazí vaše prostředí.

    Požadované prostředí bude zobrazeno jako zařazeno do fronty a potom nasazeno. Dokončení pracovních postupů prostředí bude trvat určitou dobu. Proto se vraťte přibližně za 6 až 9 hodin.

1. Než budete pokračovat, ujistěte se, že je stav prostředí **Nasazený**.

### <a name="initialize-the-commerce-scale-unit-csu"></a>Inicializace commerce scale unit (CSU)

Pokud chcete inicializovat CSU, postupujte takto.

1. V zobrazení **Prostředí hostovaná v cloudu** vyberte v seznamu požadované prostředí.
1. V zobrazení prostředí napraco vyberte **úplné podrobnosti**. Zobrazí se podrobnosti o prostředí.
1. V části **Funkce prostředí** vyberte **Spravovat**.
1. Na kartě **Velkoobchod** vyberte **Inicializovat**. Zobrazí se zobrazení inicializačních parametrů CSU.
1. V poli **Oblast** zvolte **East US**, **East US 2**, **West US** nebo **West US 2**.
1. V poli **Verze** vyberte možnost **Určit verzi** v seznamu a pak zadejte **9.18.20014.4** do zobrazeného pole. Je třeba zadat přesnou verzi, která je zde uvedena. V opačném případě bude nutné RCSU aktualizovat na správnou verzi později.
1. Zapněte možnost **použít rozšíření**.
1. V seznamu přípon vyberte možnost **Náhled rozšíření ukázky Commerce**.
1. Vyberte **Inicializovat**.
1. Na stráncee s potvrzením nasazení ověřte správnost podrobností klikněte vyberte **Ano**. Zobrazení **Správa velkoobchodu** se objeví znovu, když je vybraná karta **Commerce**. Vaše CSU byla zařazena do fronty pro zřizování.
1. Než budete pokračovat, ujistěte se, že je stav CSU **Úspěch**. Inicializace trvá přibližně dvě až pět hodin.

### <a name="initialize-e-commerce"></a>Inicializace e-Commerce

Pokud chcete inicializovat e-Commerce, postupujte takto.

1. Na kartě **e-Commerce** zkontrolujte souhlas s náhledem a pak vyberte **nastavení.**
1. Zadejte název pro **Název klienta e-Commerce**. Uvědomte si však, že název bude viditelný u některých adres URL, které odkazují na vaši instanci e-Commerce.
1. V poli **Název Commerce scale unit** vyberte položku CSU v seznamu. (Seznam by měl mít pouze jednu možnost.)

    Pole **Geografie e-Commerce** je nastaveno automaticky a hodnota nemůže být změněna.

1. Pokračujte výběrem tlačítka **Další**.
1. Do pole **Podporované názvyhostitelů** zadejte libovolnou platnou doménu, například `www.fabrikam.com`.
1.  Ve skupině **Skupina zabezpečení AAD pro správce systému** zadejte několik prvních písmen názvu skupiny zabezpečení, kterou chcete použít. Chcete-li zobrazit výsledky hledání, vyberte ikonu lupy. V seznamu vyberte správnou skupinu zabezpečení.
2.  Ve skupině **Skupina zabezpečení AAD pro moderátora hodnocení a recenzí** zadejte několik prvních písmen názvu skupiny zabezpečení, kterou chcete použít. Chcete-li zobrazit výsledky hledání, vyberte ikonu lupy. V seznamu vyberte správnou skupinu zabezpečení.
1. Ponechte možnost **Povolit službu hodnocení a recenzí** povolenou.
1. Vyberte **Inicializovat**. Zobrazení **Správa velkoobchodu** se objeví znovu, když je vybraná karta **e-Commerce**. Vaše inicializace e-Commerce byla zahájena.
1. Než budete pokračovat, počkejte, dokud nebude inicializační stav e-Commerce **Inicializace úspěšná**.
1. V **Odkazech** v pravém dolním roku si poznamenejte adresy URL následujících odkazů:

    * **Web e-Commerce** – odkaz na kořenový adresář webu e-Commerce.
    * **Nástroj pro správu webu e-Commerce** – odkaz na nástroj pro správu webu.

## <a name="commerce-preview-environment-support"></a>Podora ukázkového prostředí služby Commerce

Pokud při provádění kroků zajišťování dojde k problémům, o pomoc se obraťte na [skupinu náhledu Microsoft Dynamics 365 Commerce v aplikaci Yammer](https://aka.ms/Dynamics365CommercePreviewYammer).

## <a name="next-steps"></a>Další kroky

Chcete-li pokračovat v procesu zřizování a konfigurace prostředí náhledu Commerce, viz [Konfigurace prostředí pro náhled Commerce](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Další zdroje

[Přehled prostředí Preview aplikace Dynamics 365 Commerce](cpe-overview.md)

[Konfigurace prostředí Preview aplikace Dynamics 365 Commerce](cpe-post-provisioning.md)

[Konfigurace volitelných funkcí pro prostředí Preview aplikace Dynamics 365 Commerce](cpe-optional-features.md)

[Často kladené dotazy k prostředí Preview aplikace Dynamics 365 Commerce](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Portál Microsoft Azure](https://azure.microsoft.com/features/azure-portal)

[Web Dynamics 365 Commerce](https://aka.ms/Dynamics365CommerceWebsite)

