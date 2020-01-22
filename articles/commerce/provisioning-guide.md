---
title: Zřizování ukázkového prostředí služby Commerce
description: Toto téma vysvětluje, jak zřídit ukázkové prostředí v Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 01/06/2020
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
ms.openlocfilehash: b77d2cbbc100aeae5dcd53ddbe69ff2e4435da13
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934741"
---
# <a name="provision-a-commerce-preview-environment"></a>Zřizování ukázkového prostředí služby Commerce

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Toto téma vysvětluje, jak zřídit ukázkové prostředí v Microsoft Dynamics 365 Commerce.

Než začnete, doporučujeme, abyste celé téma alespoň zběžně pročetli, abyste získali představu o tom, co proces obnáší a co téma obsahuje.

> [!NOTE]
> Pokud ještě nemáte přístup k náhledu Dynamics 365 Commerce, můžete požádat o přístup k náhledu z [webu Commerce](https://aka.ms/Dynamics365CommerceWebsite).

## <a name="overview"></a>Přehled

Chcete-li úspěšně zřídit prostředí pro náhled Commerce, musíte vytvořit projekt, který má specifický název a typ produktu. Prostředí a Retail Cloud Scale Unit (RCSU) také mají některé specifické parametry, které musíte použít ke zřizování e-Commerce později. Pokyny v tomto tématu popisují všechny požadované kroky, které je třeba provést, a parametry, které je nutné použít.

Po úspěšném zřízení ukázkového prostředí Commerce je k přípravě prostředí náhledu nutné provést několik dalších kroků. Některé kroky jsou volitelné, v závislosti na aspektech systému, které chcete vyhodnotit. Volitelné kroky můžete vždy dokončit později.

Informace o konfiguraci prostředí pro náhled Commerce po jeho vytvoření najdete v části [konfigurace prostředí pro náhled Commerce](cpe-post-provisioning.md). Informace o konfiguraci volitelných funkcí prostředí pro náhled Commerce najdete v části [konfigurace volitelných funkcí prostředí pro náhled Commerce](cpe-optional-features.md).

Pokud máte dotazy týkající se kroků zřizování nebo pokud se vyskytnou nějaké problémy, sdělte je společnosti Microsoft na [Microsoft Dynamics 365 Commerce, skupina náhledu Yammer](https://aka.ms/Dynamics365CommercePreviewYammer).

## <a name="prerequisites"></a>Předpoklady

Aby bylo možné zřídit prostředí pro náhled Commerce, musí být zavedeny následující předpoklady:

- Máte přístup k portálu Microsoft Dynamics Lifecycle Services (LCS).
- Byli jste přijati do programu náhledu Dynamics 365 Commerce.
- Máte požadovaná oprávnění k vytvoření projektu pro **potenciální předprodej** nebo **migraci, vytvoření řešení a další informace**.
- Máte roli **Správce prostředí** nebo **Vlastník projektu** v projektu, kde se chystáte zřídit prostředí.
- Máte přístup pro správu ke svému předplatnému Microsoft Azure nebo jste v kontaktu se správcem předplatného, který může provést dva kroky, které pro vás vyžadují oprávnění správce.
- Máte k dispozici ID klienta Azure Active Directory (Azure AD).
- Vytvořili jste Skupinu zabezpečení Azure AD, kterou lze použít jako skupinu správců systému e-Commerce a máte k dispozici její ID.
- Vytvořili jste skupinu zabezpečení Azure AD, kterou lze použít jako skupinu pro moderátory hodnocení a recenzí a máte k dispozici její ID. (Tato skupina zabezpečení může být shodná se skupinou správců systému e-commerce.)

### <a name="find-your-azure-ad-tenant-id"></a>Najděte ID klienta Azure AD

ID klienta Azure AD je globálně jedinečný identifikátor (GUID), který se podobá následujícímu příkladu: **72f988bf-86f1-41af-91ab-2d7cd011db47**.

#### <a name="find-your-azure-ad-tenant-id-by-using-the-azure-portal"></a>Najděte své ID klienta Azure AD pomocí Azure portálu

1. Přihlaste se do [portálu Azure](https://portal.azure.com/).
1. Ujistěte se, zda jste vybrali správný adreář.
1. V levé nabídce vyberte **Azure Active Directory**.
1. Ve **Spravovat** vyberte **Vlastnosti**. ID klienta Azure AD se zobrazí v **ID adresáře**.

#### <a name="find-your-azure-ad-tenant-id-by-using-openid-connect-metadata"></a>Vyhledání ID klienta Azure AD pomocí metadat OpenID Connect

Vytvořte adresu URL OpenID nahrazením **\{VAšE\_DOMéNA\}** VAší doménou, například `microsoft.com`. Například `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration`  se stane `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.

1. Přejděte na adresu URL OpenID, která obsahuje vaši doménu.

    ID klienta Azure AD lze zobrazit ve více hodnotách vlastností.

1. Najděte **authorization\_endpoint** a extrahujte identifikátor GUID, který se zobrazí ihned po `login.microsoftonline.com/`.

### <a name="find-your-azure-ad-security-group-id"></a>Vyhledání ID skupiny zabezpečení Azure AD

ID skupiny zabezpečení Azure AD je identifikátor GUID, který se podobá následujícímu příkladu: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.

Tento postup předpokládá, že jste členem skupiny, pro kterou chcete najít ID.

1. Otevřete [Orůzkumník grafů](https://developer.microsoft.com/graph/graph-explorer#).
1. Vyberte **Přihlásit se k Microsoft** a přihlaste se pomocí svých pověření.
1. Vlevo vyberte možnost **zobrazit další ukázky**.
1. Povolte **Skupiny** z pravého podokna.
1. Zavřít pravé podokno.
1. Vyberte možnost **všechny skupiny, do kterých patřím**.
1. V poli **náhledu odpovědi** najděte svou skupinu. ID skupiny zabezpečení se zobrazí ve vlastnosti **ID**.

## <a name="provision-your-commerce-preview-environment"></a>Zřizování ukázkového prostředí služby Commerce

Tyto postupy vysvětlují, jak zřídit prostředí pro náhled Commerce. Po úspěšném dokončení těchto nastavení bude prostředí pro náhled Commerce připraveno na konfiguraci. Všechny popsané aktivity se objeví na portálu LCS.

> [!IMPORTANT]
> Přístup k náhledu je svázán s účtem LCS a organizací, kterou jste určili v aplikaci pro náhled. K zajištění prostředí náhledu Commerce je nutné použít stejný účet. Pokud musíte použít jiný účet LCS nebo nájemce pro prostředí náhledu Commerce, musíte tyto podrobnosti poskytnout společnosti Microsoft. Kontaktní informace naleznete v části [Podpora ukázkového prostředí Commerce](#commerce-preview-environment-support) dále v tomto tématu.

### <a name="grant-access-to-e-commerce-applications"></a>Udělení přístupu k aplikacím e-Commerce

> [!IMPORTANT]
> Osoba, která se přihlásí, musí být správcem klienta Azure AD, který má ID klienta Azure AD. Pokud tento krok není úspěšně dokončen, zbývající kroky zřízení se nezdaří.

Chcete-li autorizovat aplikace e-Commerce a získat přístup k předplatnému vašeho Azure, postupujte následovně.

1. Sestavte adresu URL v následujícím formátu:

    `https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345`

1. Zkopírujte a vložte adresu URL do prohlížeče nebo do textového editoru a nahraďte **\{AAD\_TENANT\_ID\}** vaším ID klienta Azure AD. Pak otevřete adresu URL.
1. V dialogovém okně přihlášení Azure AD se přihlaste a potvrďte, že chcete udělit přístup k předplatnému **Dynamics 365 Commerce (náhled)**. Budete přesměrováni na stránku ukazující, zda operace proběhla úspěšně.

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
> Je možné, že nebudete muset dokončit kroky 6, 7 a/nebo 8, protože stránky, které mají jedinou možnost, jsou přeskočeny. V zobrazení **Parametry prostředí** potvrďte, že se text **Dynamics 365 Commerce (Náhled)-demo (10.0.6 s aktualizací platformy 30)** zobrazuje přímo nad polem **Název prostředí**. Viz obrázek, který se zobrazí po kroku 8.

1. V horní nabídce vyberte možnost **Prostředí hostovaná v cloudu**.
1. Prostředí přidáte výběrem tlačítka **Přidat**.
1. V poli **Verze aplikace** vyberte **10.0.6**.
1. V poli **Verzi platformy** vyberte **Platform Update 30**.

    ![Vyběr verze aplikace a platformy](./media/project1.png)

1. Zvolte **Další**.
1. Výberte **Demo** jako topologii prostředí.

    ![Výběr topologie prostředí 1](./media/project2.png)

1. Vyberte **Dynamics 365 Commerce (Náhled) - Demo** jako topologii prostředí. Pokud jste dříve nakonfigurovali jeden konektor Azure Connector, bude se používat pro toto prostředí. Pokud jste nakonfigurovali více konektorů Azure, můžete vybrat, kterou spojnici chcete použít: **:Východ USA**, **Východ USA 2**, **Západ USA** nebo **Západ USA 2**. (Pro dosažení nejlepšího výkonu doporučujeme vybrat **Západ USA 2**.)

    ![Výběr topologie prostředí 2](./media/project3.png)

1. Na stránce **Nasadit prostředí** zadejte název prostředí. Ponechte Upřesňující nastavení, jak je.

    ![Stránka Nasazení prostředí](./media/project4.png)

1. Upravte velikost VM podle potřeby. (Doporučujeme skladovou jednotku VM \[SKU\] **D13 v2**.)
1. Zkontrolujte ceny a licenční podmínky a pak zaškrtnutím políčka označte, že s nimi souhlasíte.
1. Zvolte **Další**.
1. Na stráncee s potvrzením nasazení ověřte správnost podrobností klikněte vyberte **Nasadit**. Vrátíte se do zobrazení **Prostředí hostovaná v cloudu** a v seznamu se zobrazí vaše prostředí.

    Požadované prostředí bude zobrazeno jako zařazeno do fronty a potom nasazeno. Dokončení pracovních postupů prostředí bude trvat určitou dobu. Proto se vraťte přibližně za 6 až 9 hodin.

1. Než budete pokračovat, ujistěte se, že je stav prostředí **Nasazený**.

### <a name="initialize-rcsu"></a>Inicializujte RCSU

Pokud chcete inicializovat RCSU, postupujte takto.

1. V zobrazení **Prostředí hostovaná v cloudu** vyberte v seznamu požadované prostředí.
1. V zobrazení prostředí napraco vyberte **úplné podrobnosti**. Zobrazí se podrobnosti o prostředí.
1. V části **Funkce prostředí** vyberte **Spravovat**.
1. Na kartě **Maloobchod** vyberte **Inicializovat**. Zobrazí se zobrazení inicializačních parametrů RCSU.
1. V poli **Oblast** zvolte **East US**, **East US 2**, **West US** nebo **West US 2**.
1. V poli **Verze** vyberte možnost **Určit verzi** v seznamu a pak zadejte **9.16.19262.5** do zobrazeného pole. Je třeba zadat přesnou verzi, která je zde uvedena. V opačném případě bude nutné RCSU aktualizovat na správnou verzi později.
1. Zapněte možnost **použít rozšíření**.
1. V seznamu přípon vyberte možnost **Náhled rozšíření ukázky Commerce**.
1. Vyberte **Inicializovat**.
1. Na stráncee s potvrzením nasazení ověřte správnost podrobností klikněte vyberte **Ano**. Vrátíte se do zobrazení **Řízení maloobchodu** s vybranou kartou **Maloobchod**. Vaše RCSU byla zařazena do fronty pro zřizování.
1. Než budete pokračovat, ujistěte se, že je stav RCSU **Úspěch**. Inicializace trvá přibližně dvě až pět hodin.

### <a name="initialize-e-commerce"></a>Inicializace e-Commerce

Pokud chcete inicializovat e-Commerce, postupujte takto.

1. Na kartě **e-Commerce (Náhled)** zkontrolujte souhlas s náhledem a pak vyberte **nastavení.**
1. Zadejte název pro **Název klienta e-Commerce**. Uvědomte si však, že název bude viditelný u některých adres URL, které odkazují na vaši instanci e-Commerce.
1. V poli **Název Retail Cloud Scale Unit** vyberte položku RCSU v seznamu. (Seznam by měl mít pouze jednu možnost.)

    Pole **Geografie e-Commerce** je nastaveno automaticky a hodnota nemůže být změněna.

1. Pokračujte výběrem tlačítka **Další**.
1. Do pole **Podporované názvyhostitelů** zadejte libovolnou platnou doménu, například `www.fabrikam.com`.
1.  Ve skupině **Skupina zabezpečení AAD pro správce systému** zadejte několik prvních písmen názvu skupiny zabezpečení, kterou chcete použít. Chcete-li zobrazit výsledky hledání, vyberte ikonu lupy. Vyberte skupinu zabezpečení ze seznamu.
2.  Ve skupině **Skupina zabezpečení AAD pro moderátora hodnocení a recenzí** zadejte několik prvních písmen názvu skupiny zabezpečení, kterou chcete použít. Chcete-li zobrazit výsledky hledání, vyberte ikonu lupy. Vyberte skupinu zabezpečení ze seznamu.
1. Ponechte možnost **Povolit službu hodnocení a recenzí** povolenou.
1. Pokud jste již dokončili krok souhlasu společnosti Microsoft Azure Active Directory (Azure AD) podle popisu v části "Udělení přístupu k aplikacím e-Commerce", zaškrtněte políčko a potvrďte svůj souhlas. Pokud jste tento krok ještě nedokončili, musíte to provést dříve, než budete pokračovat v inicializaci. Chcete-li otevřít dialogové okno souhlasu a dokončit krok, vyberte odkaz v textu vedle zaškrtávacího políčka.
1. Vyberte **Inicializovat**. Vrátíte se do zobrazení **Řízení maloobchodu** s vybranou kartou **e-Commerce (Náhled)**. Vaše inicializace e-Commerce byla zahájena.
1. Než budete pokračovat, počkejte, dokud nebude inicializační stav e-Commerce **Inicializace úspěšná**.
1. V **Odkazech** v pravém dolním roku si poznamenejte adresy URL následujících odkazů:

    * **Web e-Commerce** – odkaz na kořenový adresář webu e-Commerce.
    * **Nástroj pro správu webu e-Commerce** – odkaz na nástroj pro správu webu.

## <a name="commerce-preview-environment-support"></a>Podora ukázkového prostředí služby Commerce

Pokud při provádění kroků zajišťování dojde k problémům, o pomoc se obraťte na [skupinu náhledu Microsoft Dynamics 365 Commerce v aplikaci Yammer](https://aka.ms/Dynamics365CommercePreviewYammer).

Pokud se při pokusu o přístup ke skupině Yammer vyskytnou problémy, můžete kontaktovat společnost Microsoft e-mailem na adrese <Dynamics365Commerce@microsoft.com>. Tato e-mailová adresa není aktivně monitorována. Proto očekávejte prodlevu v odpovědi.

## <a name="next-steps"></a>Další kroky

Chcete-li pokračovat v procesu zřizování a konfigurace prostředí náhledu Commerce, viz [Konfigurace prostředí pro náhled Commerce](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Další zdroje

[Přehled prostředí náhledu Commerce](cpe-overview.md)

[Konfigurovat prostředí náhledu Commerce](cpe-post-provisioning.md)

[Nastavení volitelných funkcí pro prostředí náhledu Commerce](cpe-optional-features.md)

[Často kladené dotazy k prostředí náhledu Commerce](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Portál Microsoft Azure](https://azure.microsoft.com/features/azure-portal)

[Web Dynamics 365 Commerce](https://aka.ms/Dynamics365CommerceWebsite)

[Zdroje nápovědy pro Dynamics 365 Retail](../retail/index.md)
