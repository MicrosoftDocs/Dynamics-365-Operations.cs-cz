---
title: Konfigurace prostředí vyhodnocení elektronického obchodování
description: Tato příručka obsahuje podrobné pokyny pro zřízení a konfiguraci prostředí náhledu aplikace Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/15/2019
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b0dce2796e69cd8dee87cba176a521c26c81eb1a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771673"
---
# <a name="configure-an-e-commerce-evaluation-environment"></a>Konfigurace prostředí vyhodnocení elektronického obchodování

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tato příručka obsahuje podrobné pokyny pro zřízení a konfiguraci prostředí náhledu aplikace Microsoft Dynamics 365 Commerce. Než začnete, doporučujeme, abyste dokumentaci alespoň zběžně pročetli, abyste získali představu o tom, co proces obnáší a co obsahuje příručka.

*Poznámka: Pokud ještě nemáte přístup k náhledu Microsoft Dynamics 365 Commerce, můžete požádat o přístup k náhledu z [webu Commerce](https://aka.ms/Dynamics365CommerceWebsite).*

## <a name="summary"></a>Souhrn
Chcete-li zajistit úspěšné zřízení prostředí, je nutné vytvořit projekt s určitým názvem a typem produktu. Prostředí a Retail Cloud Scale Unit také mají některé specifické parametry, které je třeba použít ke spuštění zřizování e-Commerce později. Pokyny v této příručce obsahují všechny požadované kroky, které je třeba provést, a parametry, které je třeba použít.

Po úspěšném zízení je k přípravě prostředí náhledu nutné provést několik dalších kroků. Některé kroky jsou volitelné, v závislosti na aspektech systému, které chcete vyhodnotit. Pokud později změníte názor, měli byste se vrátit k některému volitelnému kroku.

Pokud máte dotazy týkající se kroků zřizování nebo pokud se vyskytnou nějaké problémy, sdělte nám na [Microsoft Dynamics 365 Commerce, skupina náhledu Yammer](https://aka.ms/Dynamics365CommercePreviewYammer). 

## <a name="prerequisites"></a>Předpoklady
Následují předpoklady pro zřízení vašeho ukázkového prostředí Dynamics 365:
* Máte přístup k **portálu Lifecycle Services (LCS)**
* Byli jste **přijati do programu Dynamics 365 Commerce Preview.**
* Máte požadovaná oprávnění k vytvoření projektu pro **potenciální předprodej** nebo **migraci, vytvoření řešení a další informace.**
* Máte roli **Správce prostředí** nebo **Vlastník projektu** v projektu, kde se chystáte zřídit prostředí.
* Máte přístup pro správu ke svému předplatnému Azure nebo se obraťte na správce předplatného, který může provést dva kroky, které pro vás vyžadují oprávnění správce.
* Máte k dispozici **ID klienta AAD**.
* Vytvořili jste **Skupinu zabezpečení AAD**, kterou chcete použít jako **Skupinu správců systému e-Commerce** a máte k dispozici její ID.
* Vytvořili jste **Skupinu zabezpečení AAD**, kterou chcete použít jako **Skupinu moderátorů hodnocení a recenzí** a máte k dispozici její ID (může se jednat o skupinu zabezpečení jako je skupina správců systému výše).
## <a name="provisioning-preview-environment"></a>Zřizování ukázkového prostředí
Tyto pokyny pokrývají zřizování ukázkového prostředí Microsoft Dynamics 365 Commerce. Po úspěšném dokončení těchto kroků budete mít k dispozici náhled prostředí, které je připraveno ke konfiguraci. Všechny popsané aktivity se uskuteční na portálu LCS.

*Všimněte si, že přístup k náhledu je svázán s účtem LCS a organizací, které jste zadali v aplikaci pro náhled. Stejný účet je třeba použít pro zřizování. Pokud je pro prostředí náhledu nutné použít jiný účet LCS nebo klienta, je třeba nám tyto podrobnosti sdělit. Informace o kontaktech naleznete níže v části Další zdroje.*
### <a name="before-starting"></a>Před zahájením
##### <a name="grant-access-to-e-commerce-applications"></a>Udělení přístupu k aplikacím e-Commerce

*Poznámka: **přihlášený uživatel musí mít oprávnění správce klienta AAD**. Pokud úspěšně neprovedete tento krok, zbytek kroků zajišťování se nezdaří.*

1. V tomto kroku budete potřebovat vaše **ID klienta AAD**. Chcete-li získat přístup k předplatnému Azure, musíte autorizovat aplikace e-Commerce. Nejjednodušší je sestavit adresu URL takto:

https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345

2. **Neklikejte na adresu URL přímo**, zkopírujte ji a vložte ji do prohlížeče nebo textového editoru a nahraďte **\{AAD_TENANT_ID\}** vaším **ID klienta AAD**, než přejdete na adresu URL.
3. Zobrazí se přihlašovací dialogové okno služby Microsoft AAD, ve kterém potvrdíte, že chcete udělit přístup Dynamics 365 Commerce (Preview) k předplatnému.
4. Zobrazí se stránka potvrzující, zda operace proběhla úspěšně.

##### <a name="log-in-to-the-lcs"></a>Přihlaste se k systému LCS
1. Přihlaste se k portálu LCS: https://lcs.dynamics.com
1. Ujistěte se, že jste přihlášeni se stejným účtem LCS, který jste použili při požadavku na přístup k náhledu.
##### <a name="confirm-that-preview-features-are-available-and-enabled"></a>Zkontrolujte, zda jsou k dispozici funkce náhledu a zda jsou povoleny.
1. Na titulní stránce LCS posuňte se úplně doprava a klepněte na dlaždici **Správa funkcí náhledu**.
1. Posuňte se dolů k „Funkcím soukromé verze Preview“ a zkontrolujte, zda jsou dostupné a povolené následující funkce:
    1. **Hodnocení e-Commerce**
    1. **Prostředí služby Commerce Preview**
1. Pokud tyto funkce nevidíte v seznamu, spojte se s námi pomocí pracovního e-mailu, s účtem LCS a podrobnostmi o klientu. Další informace o tom, jak nás kontaktovat, naleznete v **Dalších zdrojích**.

![Dlaždice správy verze Preview](./media/preview1.png)

![Ukázkové funkce](./media/preview2.png)
### <a name="create-project"></a>Vytvořit projekt
##### <a name="creating-new-project"></a>Vytvoření nového projektu
1. Klikněte na **+** pro vytvoření nového projektu.
1. Pokud jste partnerem, zvolte možnost **Migrovat, vytvořit řešení a získat informace**.
1. Pokud jste odběratel, vyberte možnost **Potenciální předprodeje**.
1. Zadejte název, popis a odvětví podle potřeby.
1. V **Názvu produktu** vyberte **Dynamics 365 Retail**.
1. Ve **Verzi produktu** vyberte **Dynamics 365 Retail**.
1. V **metodologii** vyberte **Metodologiin implementace Dynamics Retail**.
1. V případě potřeby můžete z existujícího projektu importovat role a uživatele.
1. Klepněte na volbu **Nový**.
1. Jste odesláni do zobrazení projektu.
##### <a name="add-azure-connector"></a>Přidejte konektor Azure
1. Pokud jste partnerem, klikněte na možnost **Nastavení projektu** na dlaždici nástrojů zcela vpravo.
1. Pokud jste odběratel, zvolte **Nastavení projektu** z horní nabídky.
1. Vyberte **Konektory Azure**.
1. Chcete-li přidat konektor Azure, klikněte na tlačítko **+ Přidat**.
1. Zadejte název.
1. Vložte své **ID předplatného Azure**.
1. Povolte **Konfigurovat pro použití technologie ARM (Azure Resource Manager)**.
1. Ověřte správnost **Domény klienta předplatného služby Azure AAD ( nebo ID)**. V případě potřeby se obraťte na správce předplatného Azure.
1. Klepněte na tlačítko **Další**.
1. Podle pokynů na obrazovce udělte požadovaným aplikacím přístup k vašemu předplatnému. V případě potřeby se obraťte na správce předplatného Azure:
    1. Přihlaste se k portálu Azure: https://portal.azure.com/
    1. Ujistěte se, zda jste vybrali správný adreář.
    1. Klepněte na **Předplatné** v nabídce vlevo.
    1. Vyhledejte správné předplatné ze seznamu a vyberte je. V případě potřeby použijte hledání.
    1. V nabídce vyberte **Řízení přístupu (IAM)**.
    1. Klikněte na **Přidat** v části **Přidat přiřazení role** na pravé straně. Otevře se podokno **Přidat přiřazení role**.
    1. V případě **role** vyberte **Přispěvatel**.
    1. Možnost **Přiřadit přístup k** ponechte jako **uživatel, skupina nebo hlavní název služby Azure AD**.
    1. V možnosti **Vybrat** vložte **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.
    1. Vyberte **Služba pro nasazení aplikace Dynamics [wsfed-enabled]** ze seznamu.
    1. Klikněte na možnost **Uložit**.
1. Klepněte na tlačítko **Další**.
1. Podle pokynů na obrazovce udělte požadovaným aplikacím přístup k vašemu předplatnému. V případě potřeby se obraťte na správce předplatného Azure.
1. Klepněte na tlačítko **Další**.
1. Pro **Oblast Azure** zvolte **East US**, **East US 2**, **West US** nebo **West US 2**.
1. Klepněte na tlačítko **Připojit**.
1. V seznamu by se měl zobrazit konektor Azure.
### <a name="import-extension"></a>Rozšíření importu
1. Přejděte zpět na titulní atránku projektu klepnutím na název projektu na horním okraji.
1. Pokud jste partnerem, klikněte na možnost **Knihovna majetku** na dlaždici nástrojů zcela vpravo.
1. Pokud jste odběratel, zvolte **Knihovna majetku** z horní nabídky.
1. Ze seznamu vlevo vyberte **Balíček nasazení softwaru**.
1. V podokně akcí klikněte na možnost **IMPORT**.
1. Vyberte **Náhled rozšíření ukázky Commerce** v seznamu majetku v možnosti **KNIHOVNA SDíLENéHO MAJETKU**.
1. Klikněte na **Vybrat**.
1. Vrátíte se do knihovny majetku a toto rozšíření se zobrazí v seznamu.

![Vytváření projektu - verze](./media/import.png)
### <a name="deploy-environment"></a>Nasazení prostředí

*Poznámka: je možné, že kroky 6, 7 a/nebo 8 nebudou zobrazeny, protože jsou přeskočeny obrazovky s jednou možností. Pokud se nacházíte v zobrazení **Parametry prostředí**, potvrďte, že máte text "Dynamics 365 Commerce (Preview) - demo (10.0.6 s aktualizací platformy 30)" přímo nad polem **Název prostředí**. Viz snímek obrazovky níže.*

1. V horní nabídce vyberte možnost **Prostředí hostovaná v cloudu**.
1. Prostředí přidáte klepnutím na tlačítko **+ Přidat**.
1. Ve **Verzi aplikace** vyberte **10.0.6**.
1. Jako **Verzi platformy** vyberte **Platform Update 30**.
1. Klepněte na tlačítko **Další**.
1. V případě topologie prostředí vyberte **DEMO**.
1. V případě topologie prostředí vyberte **Dynamics 365 Commerce (Preview) - Demo**.
1. Pokud jste dříve nakonfigurovali jeden konektor Azure Connector, bude se používat pro toto prostředí. Pokud jste nakonfigurovali více konektorů Azure, máte možnost vybrat konektor, který chcete použít: **východ USA**, **východ USA 2**, **západ USA** nebo **západ USA 2** (doporučeno pro nejlepší výkon)
1. Zadejte **Název prostředí**.
1. Podle potřeby upravte velikost virtuálního počítače. (Doporučujeme VM SKU **D13 v2**.)
1. Ponechte **Upřesňující nastavení**, jak je.
1. Po kontrole smlouvy o cenách a licenčních podmínkách na obrazovce zaškrtněte políčko a určete smlouvu.
1. Klepněte na tlačítko **Další**.
1. Na obrazovce s potvrzením nasazení po ověření správnosti podrobností klikněte na tlačítko **Nasadit.**
1. Vrátíte se do zobrazení **Prostředí hostovaná v cloudu** a v seznamu se zobrazí vaše prostředí.
1. Požadované prostředí bude zobrazeno jako zařazeno do fronty a potom nasazeno. Dokončení všech pracovních postupů prostředí bude chvíli trvat, takže se vraťte zpět po několika hodinách (přibližně 6 – 9 hodin).
1. Než budete pokračovat, ujistěte se, že je stav prostředí **Nasazený**.

![Vytváření projektu - verze](./media/project1.png)

![Vytváření projektu - topologie 1](./media/project2.png)

![Vytváření projektu - topologie 2](./media/project3.png)

![Vytvoření projektu – parametry prostředí](./media/project4.png)
### <a name="initialize-rcsu"></a>Inicializujte RCSU
1. V zobrazení **Prostředí hostovaná v cloudu** vyberte v seznamu požadované prostředí.
1. V zobrazení prostředí na pravé straně obrazovky klikněte na možnost **Úplné podrobnosti**. Zobrazí se podrobnosti o prostředí.
1. V části **FUNKCE PROSTřEDí** klepněte na možnost **spravovat**.
1. Na kartě **Retail** klikněte na **Inicializovat**. Zobrazí se zobrazení inicializačních parametrů RCSU.
1. Jako **OBLAST** zvolte **East US**, **East US 2**, **West US** nebo **West US 2**.
1. V případě **VERZE** vyberte nejprve **Zadat verzi** z rozevíracího seznamu a poté zadejte **9.16.19262.5** do pole text, které se zobrazí níže. *Poznámka: Zkontrolujte, zda je zde **uvedena přesná verze**, abyste nemuseli aktualizovat RCSU později na správnou verzi.*
1. Povolit **Použít rozšíření**.
1. V seznamu přípon vyberte možnost **Náhled rozšíření ukázky Commerce**.
1. Klepněte na tlačítko **Inicializovat**.
1. Na obrazovce s potvrzením nasazení po ověření správnosti podrobností klikněte na tlačítko **Ano**.
1. Vrátíte se do zobrazení **Řízení maloobchodu** s aktivovanou kartou **Maloobchod**. Vaše RCSU byla zařazena do fronty pro zřizování.
1. Před pokračováním počkejte, dokud nebude stav RCSU **ÚSPěCH** (bude to trvat přibližně 2-5 hodin).
### <a name="initialize-e-commerce"></a>Inicializace e-Commerce
1. Přejděte na kartu **e-Commerce (Preview)**.
1. Po kontrole souhlasu s náhledem klikněte na **Nastavení**.
1. Zadejte název pro **Název klienta e-Commerce**. Uvědomte si však, že tato akce bude viditelná u některých adres URL, které odkazují na vaši instanci e-Commerce.
1. Pro **název Retail cloud scale unit** vyberte ze seznamu RCSU (seznam by měl mít pouze jednu možnost).
1. **Geografie e-Commerce** je vyplněna automaticky a nelze ji změnit.
1. Pokračujte klepnutím na tlačítko **Další**.
1. Pro **Podporované názvy hostitelů** zadejte libovolnou platnou doménu (např. www.fabrikam.com).
1. Jako **Skupinu zabezpečení AAD pro správce systému** zadejte AAD SG ID, které chcete použít jako skupinu správy systému e-Commerce.
1. Jako **Skupinu zabezpečení AAD pro moderátora hodnocení a recenzí** zadejte AAD SG ID, které chcete použít jako skupinu moderátorů hodnocení a recenzí.
1. Ponechte hodnoty **B2C** prázdné (7 polí začínajících na B2C).
1. Ponechte **Povolit službu hodnocení a recenzí** povoleno.
1. Klepněte na tlačítko **Inicializovat**.
1. Vrátíte se do zobrazení **Řízení maloobchodu** s aktivovanou kartou **e-Commerce (Preview)**. Vaše inicializace e-Commerce byla zahájena.
1. Než budete pokračovat, počkejte, dokud nebude inicializační stav e-Commerce **INICIALIZACE úSPěšNá**.
1. V části **ODKAZY** vpravo dole.
    * Poznamenejte si odkaz **webu e-Commerce**. Toto je odkaz na kořenovou složku webu C2.
    * Poznamenejte si odkaz **nástroje pro správu webu e-Commerce**. Toto je odkaz na nástroj Správa webu (vytváření obsahu C1).
## <a name="post-provisioning-steps"></a>Kroky po zřízení
V této fázi bylo prostředí kompletně zřízeno, ale přesto existují kroky konfigurace, které je nutné před zahájením vyhodnocování prostředí provést.
### <a name="before-starting"></a>Před zahájením
1. V horní nabídce vyberte možnost **Prostředí hostovaná v cloudu**.
1. V seznamu vyberte své prostředí.
1. Klikněte na možnost **úplné podrobnosti** z informací o prostředí napravo.
1. Kliknutím na **Přihlásit** otevřete nabídku a vyberte **Přihlásit se k prostředí**.

Ujistěte se, že je vybrána právnická osoba **USRT** (pravý horní roh).

### <a name="configure-pos"></a>Konfigurovat frontu POS
##### <a name="associate-worker-with-your-identity"></a>Přidružit pracovníka k vaší identitě
1. Pomocí nabídky vlevo přejděte na **Moduly > Retail > Zaměstnanci > Pracovníci**.
1. Vyhledejte na seznamu áznam **000713 - Andrew Collette** a vyberte ho.
1. V podokně akcí klikněte na možnost **Maloobchod.**
1. Klikněte na **Stávající identita přidružení**.
1. Do pole **E-mail** (vpravo od **Hledání pomocí e-mailu**) zadejte svou e-mailovou adresu.
1. Klikněte na **Hledat**.
1. Vyberte záznam s vaším jménem.
1. Klikněte na tlačítko **OK**.
1. Klikněte na možnost **Uložit**.
##### <a name="activate-cloud-pos"></a>Aktivovat Cloud POS
1. Přihlaste se k portálu LCS.
1. Přejděte do svého projektu.
1. V horní nabídce vyberte možnost **Prostředí hostovaná v cloudu**.
1. V seznamu vyberte své prostředí.
1. Klikněte na možnost **úplné podrobnosti** z informací o prostředí napravo.
1. Kliknutím na tlačítko **Přihlášení** otevřete nabídku, vyberte **Přihlásit se ke cloudovému pokladnímu místu**, POS by měla být načtena.
1. Klepněte na tlačítko **Další**.
1. Přihlaste se pomocí svého účtu AAD.
1. V poli **Název obchodu** vyberte **San Francisco**.
1. Klepněte na tlačítko **Další**.
1. V **Registr a zařízení** vyberte **SANFRAN-1**.
1. Klepněte na tlačítko **Aktivovat**.
1. Měli byste být odhlášeni a skončit na obrazovce přihlášení POS.
1. Nyní se můžete přihlásit ke cloudovému POS pomocí ID operátoru **000713** a hesla **123**.
### <a name="site-setup"></a>Nastavení webu
1. Přihlaste se k **nástroji pro správu webu** pomocí adresy URL, kterou jste si poznamenali dříve.
1. Klepnutím na web **Fabrikam** otevřete dialogové okno nastavení webu.
1. V poli doména vyberte doménu, kterou jste zadali dříve při inicializaci elektronického obchodu.
1. Pro výchozí kanál vyberte **Rozšířený online obchod společnosti Fabrikam**. *Poznámka: Zkontrolujte, zda jste vybrali **rozšířený** online obchod.*
1. Pro výchozí jazyk vyberte možnost **en-us**.
1. Ponechte **Cestu** tak, jak je.
1. Klikněte na tlačítko **OK**.
1. Budete odesláni do seznamu stránek na webu.
### <a name="enable-jobs"></a>Povolit úlohy
1. Přihlaste se k prostředí (HQ).
1. Pomocí nabídky vlevo přejděte do **Retail > Dotazy a sestavy > Dávkové úlohy**.
1. Proveďte následující kroky pro každou úlohu v seznamu níže:
    * **Zpracovat maloobchodní oznámení objednávky e-mailem**.
    * **Dostupnost produktu**.
    * **P-0001**.
    * **Synchronizovat úlohu objednávek**.
1. Pomocí rychlého filtru vyhledejte úlohu pomocí jejího názvu (uvedeného výše).
1. Je-li stav úlohy nastaven na **Srážka**, proveďte následující kroky:
    1. Vybrat záznam.
    1. V podokně akcí otevřete pás **Dávková úloha** a klikněte na položku **Změnit stav**.
    1. Vyberte **Čekající** a klikněte na **OK**.
### <a name="run-full-data-sync"></a>Spustit úplnou synchronizaci dat
1. Pomocí nabídky v levé části přejděte na **Moduly > Retail > Nastavení centrály > Maloobchodní plánovač > Databáze kanálů**.
1. **Výchozí** kanál je vybrán ze seznamu vlevo. *Vyberte jiný dostupný kanál (nazvaný **scXXXXXXXXX**).*
1. V podokně akcí klepněte na volbu **Úplná synchronizace dat**.
1. Jako plán distribuce zadejte **9999**.
1. Klikněte na tlačítko **OK**.
1. Klikněte na tlačítko **OK**.
### <a name="after-these-steps-you-are-ready-to-start-evaluating-your-preview-environment"></a>Po provedení těchto kroků můžete začít s vyhodnocením prostředí náhledu.
Pomocí adresy URL **nástroje pro správu webu e-Commerce** přejděte na modul C1 a adresu URL **webu e-Commerce** pro přechod na web C2.

## <a name="additional-resources"></a>Další zdroje
### <a name="how-to-find-your-aad-tenant-id"></a>Jak najít ID klienta AAD
ID klienta AAD je identifikátor GUID a vypadá jako v následujícím příkladu: **72f988bf-86f1-41af-91ab-2d7cd011db47**
##### <a name="from-azure-portal"></a>Z Portálu Azure
1. Přihlaste se k portálu Azure: https://portal.azure.com/
1. Ujistěte se, zda jste vybrali správný adreář.
1. Klikněte na **Azure Active Directory** v nabídce vlevo.
1. Vyberte **Vlastnosti** ve **Spravovat**.
1. ID klienta AAD je uvedeno v **ID adresáře**.
##### <a name="from-openid-connect-metadata"></a>Z metadat OpenID Connect
Vytvořte **OpenID URL** tak, že nahradíte **\{YOUR_DOMAIN\}** vaší doménou, např. microsoft.com: https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration bude vypadat takto: https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration

1. Přejděte k **adrese URL OpenID** s vaší doménou.
1. ID klienta AAD lze zobrazit ve více hodnotách vlastností.
1. Vyhledejte **authorization_endpoint** a extrahujte identifikátor GUID přímo za **login.microsoftonline.com/**.
### <a name="how-to-find-the-id-of-your-aad-security-group"></a>Jak najít ID skupiny zabezpečení AAD
ID skupiny zabezpečení AAD je identifikátor GUID a vypadá jako v následujícím příkladu: **436ea7f5-ee6c-40c1-9f08-825c5811066a**

Tento krok předpokládá, že uživatel je členem skupiny, pro kterou se pokouší vyhledat ID.
1. Přejděte do Průzkumníka grafů: https://developer.microsoft.com/en-us/graph/graph-explorer#
1. Klepněte na položku **Přihlásit se k Microsoft** a přihlaste se pomocí svých pověření.
1. Po přihlášení klepněte na možnost **Zobrazit více ukázek** nalevo.
1. Povolte **Skupiny** z pravého podokna.
1. Zavřít pravé podokno.
1. Klepněte na možnost **všechny skupiny, do kterých patřím**.
1. Vyhledejte skupinu z textového pole **Náhled odpovědi**.
1. ID skupiny zabezpečení je uvedeno pod **ID** vlastnosti.
### <a name="test-credit-card-information-to-perform-test-purchases"></a>Testovat informace o kreditní kartě za účelem provedení testových nákupů
Chcete-li provést testovací transakce na webu, můžete použít tuto testovací kreditní kartu:

Číslo karty: 4111-1111-1111-1111, vypršení platnosti: 10/20, CVV: 737

*Poznámka: v žádném případě byste neměli používat informace o skutečné kreditní kartě na testovacím webu.*
### <a name="useful-links"></a>Užitečné odkazy
* [LCS (Lifecycle services)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)
* [RCSU (Retail Cloud Scale Unit)](https://docs.microsoft.com/en-us/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)
* [Portál Microsoft Azure](https://azure.microsoft.com/en-us/features/azure-portal)
* [Web Dynamics 365 Commerce](https://aka.ms/Dynamics365CommerceWebsite)
* [Zdroje nápovědy pro Dynamics 365 Retail](../retail/index.md)
### <a name="microsoft-dynamics-365-commerce-preview-support"></a>Skupina podpory Microsoft Dynamics 365 Commerce
Pokud při provádění kroků zajišťování dojde k problémům, obraťte se na skupinu [skupinu náhledu Microsoft Dynamics 365 Commerce v aplikaci Yammer](https://aka.ms/Dynamics365CommercePreviewYammer). 

Pokud máte problémy s přístupem ke skupině Yammer, můžete také kontaktovat e-mailem na **Dynamics365Commerce@microsoft.com.** Tato e-mailová adresa není aktivně sledována, a proto by byla očekávána prodleva v odpovědi.
***
## <a name="prerequisites-for-optional-features"></a>Předpoklady pro volitelné funkce
Chcete-li vyhodnotit funkce transakčního e-mailu, musí být splněny následující předpoklady:
* Máte k dispozici e-mailový server (server SMTP), který lze použít z předplatného Azure, kde zřizujete prostředí náhledu.
* Máte k dispozici název FQDN/IP, číslo portu a podrobnosti o ověřování.

Chcete-li vyhodnotit funkce správy digitálních materiálů, konkrétně požití nových omnikanálových obrázků, musí být splněny následující předpoklady:
* Je nutné mít k dispozici **název klienta CMS**. Pokyny pro vyhledání tohoto jména jsou uvedeny níže.
### <a name="configure-image-backend-optional"></a>Konfigurace bitové kopie back-end (volitelné)
##### <a name="finding-your-media-base-url"></a>Hledání základní adresy URL média
*Poznámka: před dokončením tohoto kroku je nutné dokončit **Nastavení webu**.*
1. Přihlaste se k nástroji pro správu webu pomocí adresy URL, kterou jste si poznamenali dříve.
1. Otevřete stránku **Fabrikam**.
1. Vyberte **Majetky** v nabídce vlevo.
1. Vyberte libovolný obrázek.
1. Vyhledat **veřejnou adresu URL** z inspektoru vlastností vpravo. Obsahuje adresu URL.
    * Příklad adresy URL: https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC
1. Nahraďte poslední identifikátor v adrese URL (MA1nQC ve výše uvedené ukázkové adrese URL) následujícím řetězcem: **search?fileName=**
    * Příklad adresy URL po nahrazení: https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=
    * Toto je vaše **Základní adresa URL média** – Poznamenejte si ji.
##### <a name="updating-the-media-base-url"></a>Aktualizovat základní adresu URL média
1. Přihlaste se k prostředí (HQ).
1. Pomocí nabídky v levé části přejděte na **Moduly > Retail > Nastavení kanálu > Profily kanálu**.
1. Klikněte na možnost **Upravit**.
1. Z  **vlastností profilu** nahraďte hodnotu vlastnosti pro **základní adresu URL serveru média** **základní adresou URL média**, kterou jste vytvořili dříve.
1. Vyberte jiný kanál ze seznamu vlevo pod **výchozím** kanálem.
1. Ve **Vlastnostech profilu** klikněte na **+ Přidat**.
1. Pro přidanou vlastnost vyberte jako klíč vlastnosti **základní adresu URL serveru médií** a pro hodnotu vlastnosti zadejte **základní adresu URL média**, kterou jste vytvořili dříve.
1. Klikněte na možnost **Uložit**.

### <a name="configure-email-server-optional"></a>Konfigurovat e-mailový server (volitelné)
Uvědomte si, že server SMTP nebo zadaná e-mailová služba musí být v rámci předplatného Azure, které používáte pro dané prostředí, přístupné.
1. Přihlaste se k prostředí (HQ).
1. Pomocí nabídky v levé části přejděte na **Moduly > Retail > Nastavení centrály > Parametry > Parametry e-mailu**.
1. Klikněte na kartu **Nastavení SMTP**.
1. Do **pole Server odchozí pošty** zadejte FQDN nebo adresu IP serveru SMTP nebo e-mailové služby.
1. Do pole **číslo portu SMTP** zadejte číslo portu (výchozí hodnota je 25, pokud nepoužíváte protokol SSL).
1. Do pole **uživatelské jméno** zadejte hodnotu (pokud je vyžadováno ověření).
1. Do pole **heslo** zadejte hodnotu (pokud je vyžadováno ověření).
1. Klikněte na možnost **Uložit**.
1. Klikněte na možnost **Aktualizovat**.
1. Klepněte na kartu **Testovací e-mail**.
1. V poskytovatel e-mailu vyberte **SMTP**.
1. V poli **příjemce** zadejte e-mailovou adresu, které má být doručen testovací e-mail.
1. Klikněte na **poslat tetovací e-mail**.
### <a name="configure-email-templates-optional"></a>Konfigurovat e-mailové šablony (volitelné)
Šablona e-mailu pro každou transakční událost, pro kterou chcete odeslat e-maily, musí být aktualizována platnou e-mailovou adresou odesílatele.
1. Pomocí nabídky v levé části přejděte na **Moduly > Správa organizace > Nastavení > Šablony e-mailu organizace**.
1. Klikněte na možnost **Zobrazit seznam.**
1. Pro každou šablonu v seznamu:
    1. Do pole **E-mail odesílatele** zadejte e-mailovou adresu odesílatele pro tuto šablonu e-mailu.
    1. Dobrovolné Do pole **Jméno odesílatele** zadejte název, který bude použit jako odesílatel pro tuto šablonu e-mailu.
1. Klikněte na možnost **Uložit**.
### <a name="customizing-email-templates-optional"></a>Přizpůsobení e-mailové šablony (volitelné)
Šablony e-mailů můžete upravit tak, aby používaly různé obrázky, nebo aktualizovat propojení v šabloně, aby bylo možné propojení vrátit do prostředí náhledu. Níže uvedené kroky vysvětlují, jak stáhnout výchozí šablony, přizpůsobit je a aktualizovat šablony v systému.
1. V prohlížeči můžete stáhnout [soubor .zip s náhledem výchozích šablon e-mailu Microsoft Dynamics 365 Commerce](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip), které obsahují následující dokumenty HTML v místním počítači.
    1. Šablona potvrzení objednávky
    1. Šablona dárkového poukazu
    1. Šablona nové objednávky
    1. Šablona objednávky balení
    1. Šablona objednávky výdeje
1. Přizpůsobte šablony pomocí textu nebo editoru HTML. Viz níže uvedený seznam podporovaných tokenů.
1. Přihlaste se k prostředí (HQ).
1. Pomocí nabídky v levé části přejděte na **Moduly > Retail > Nastavení centrály > Parametry > Šablony e-mailu organizace**.
1. Rozbalením seznamu v levé části zobrazíte všechny šablony.
1. Pro každou šablonu, kterou chcete přizpůsobit, proveďte následující kroky:
    1. Vyberte šablonu v seznamu.
    1. V **Obsahu e-mailové zprávy** vyberte odpovídající jazykovou verzi ze seznamu (výchozí **en-us**).
    1. V **Obsahu e-mailové zprávy** klikněte na **Upravit**. Mělo by se otevřít podokno **Nahrát e-mailovou šablonu**.
    1. Kliněte na **Procházet** a vyhledejte soubor HTML s vlastním obsahem.
    1. Klikněte na **Nahrát**, šablona je odeslána do systému a zobrazí se náhled.
    1. Klikněte na tlačítko **OK**.
    1. (Volitelné) Upravte vlastnost **Předmětu** šablony.
    1. Klikněte na možnost **Uložit**.

#### <a name="supported-tokens-in-the-email-template"></a>Podporované tokeny v šabloně e-mailu
Tyto tokeny budou nahrazeny časem zorbazení e-mailu a skutečnými hodnotami platnými pro odběratele a jejich objednávkami.

**Prodejní objednávka** – následující tokeny se vztahují na celkovou prodejní objednávku.

|Název tokenu|Token |
|---|---|
|Číslo objednávky|%salesid%|
|Jméno zákazníka|%customername%|
|Adresa dodání|%deliveryaddress%|
|Fakturační adresa|%customeraddress%|
|Datum objednávky|%shipdate%|
|Způsob doručení|%modeofdelivery%|
|Sleva|%discount%|
|DPH|%tax%|
|Celková hodnota objednávky|%total%|

**Řádek prodeje** – následující tokeny jsou vyplněny pro každý produkt v objednávce.

*Poznámka: Umístěte tokeny **seznamu produktů – začátek** a **seznamu produktů – konec** na začátku a na konci bloku HTML, který se opakuje u každého produktu.*

|Název tokenu|Token |
|---|---|
|Seznam produktů - začátek|\<!--%tablebegin.salesline% -->|
|Seznam produktů - konec|\<!--%tableend.salesline%-->|
|Název produktu|%lineproductname%|
|Popis|%lineproductdescription%|
|Množství|%linequantity%|
|Cena řádkové jednotky|%lineprice% (verify)|
|celkem řádkových položek|%linenetamount%|
|řádková sleva|%linediscount%|
|Datum expedice|%lineshipdate%|
|Způsob zásobování|%linedeliverymode%|
|adresa dodání|%linedeliveryaddress%|
|Prodejní jednotka řádku|%lineunit%|

