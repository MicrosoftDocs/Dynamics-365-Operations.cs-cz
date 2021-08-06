---
title: Obecné řešení potíží
description: Toto téma obsahuje všeobecné informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: b4de461d26fc6d5c39c1ac0c49201f265f562f5a
ms.sourcegitcommit: f65bde9ab0bf4c12a3250e7c9b2abb1555cd7931
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/13/2021
ms.locfileid: "6542484"
---
# <a name="general-troubleshooting"></a>Obecné řešení potíží

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Toto téma obsahuje všeobecné informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Dataverse.

> [!IMPORTANT]
> Některé problémy, které toto téma řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD). Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a>Při pokusu o instalaci balíčku dvojího zapisování pomocí nástroje package deployer se nezobrazí žádná dostupná řešení

Některé verze nástroje package deployer nejsou kompatibilní s balíčkem řešení dvojího zápisu. Chcete-li úspěšně nainstalovat balíček, je nutné použít [verzi 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) nebo novější z nástroje package deployer.

Po instalaci nástroje package deployer nainstalujte balíček řešení pomocí následujících kroků.

1. Stáhněte si nejnovější soubor balíčku řešení z Yammer.com. Po stažení souboru ZIP balíčku klepněte na něj pravým tlačítkem myši a vyberte **Vlastnosti**. Zaškrtněte políčko **odblokovat** a vyberte **Použít**. Není-li zaškrtávací políčko **Odblokovat** zobrazeno, je již zrušeno blokování souboru zip a tento krok můžete přeskočit.

    ![Dialogové okno Vlastnosti.](media/unblock_option.png)

2. Extrahujte soubor zip balíčku a zkopírujte všechny soubory ve složce **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438.**

    ![Obsah složky Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438.](media/extract_package.png)

3. Vložte všechny zkopírované soubory do složky **Nástroje** v nástroji Package Deployer. 
4. Spuštěním **PackageDeployer.exe** vyberte prostředí Dataverse a nainstalujte řešení.

    ![Obsah složky Nástroje.](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Chcete-li zobrazit podrobnosti chyby, povolte a zobrazte protokol sledování modulů plug-in v Dataverse

**Požadovaná role pro zapnutí protokolu sledování a zobrazení chyb:** správce systému

Chcete-li zapnout protokol sledování, postupujte následujícím způsobem.

1. Přihlaste se k aplikaci customer engagement, otevřete stránku **Nastavení** a v části **Systém** vyberte možnost **Správa**.
2. Na stránce **Správa** zvolte **Nastavení systému**.
3. Na kartě **Vlastní nastavení** ve sloupci **Modul plug-in a vlastní sledování aktivity workflowu** vyberte možnost **Vše**, chcete-li povolit trasovací protokol modulu plug-in. Chcete-li protokolovat protokoly trasování pouze při výskytu výjimek, můžete namísto toho vybrat **Výjika**.


Chcete-li zobrazit protokol sledování, postupujte následujícím způsobem.

1. Přihlaste se k aplikaci customer engagement, otevřete stránku **Nastavení** a v části **Vlastní nastavení** vyberte možnost **Protokol sledování modulu plug-in**.
2. Najděte protokoly sledování, kde sloupec **Název typu** je nastaven na **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.
3. Chcete-li zobrazit úplný protokol, klikněte dvakrát na položku, a potom na pevné záložce **Spuštění** zkontrolujte text **Message Block**.

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Povolit režim ladění pro řešení potíží se živými synchronizacemi v aplikacích Finance and Operations

**Požadovaná role pro zobrazení chyb:** Chyby duálního zápisu správce systému, které vznikly v Dataverse, se mohou objevit v aplikaci Finance and Operations. V některých případech není úplný text chybové zprávy k dispozici, protože zpráva je příliš dlouhá nebo obsahuje osobní identifikační údaje (PII). Pomocí následujících kroků můžete zapnout podrobné protokolování chyb.

1. Všechny konfigurace projektu v aplikacích Finance and Operations mají vlastnost **IsDebugMode** v tabulce **DualWriteProjectConfiguration**. Otevřete tabulku **DualWriteProjectConfiguration** pomocí doplňku aplikace Excel.

    > [!TIP]
    > Snadným způsobem, jak tuto tabulku otevřít, je zapnout režim **Návrh** v doplňku aplikace Excel a poté přidat **DualWriteProjectConfigurationEntity** do listu. další informace získáte v tématu [Otevření dat tabulky v aplikaci Excel a jejich aktualizace pomocí doplňku aplikace Excel](../../office-integration/use-excel-add-in.md).

2. Nastavte vlastnost **IsDebugMode** na **Ano** pro projekt.
3. Spuštění scénáře generujících chyby.
4. Podrobné protokoly jsou k dispozici v tabulce DualWriteErrorLog. Chcete-li vyhledat data v prohlížeči tabulky, použijte následující adresu URL (nahraďte **XXX**):

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Zkontrolujte chyby synchronizace ve virtuálním počítači pro aplikaci Finance and Operations

**Požadovaná role pro zobrazení chyb:** Správce systému

1. Přihlaste se do Microsoft Dynamics Lifecycle Services (LCS).
2. Otevřete projekt LCS, který jste zvolili pro testování dvojího zápisu.
3. Zvolte dlaždici **Prostředí hostovaná v cloudu**.
4. Pomocí vzdálené plochy se přihlaste k virtuálnímu počítači (VM) pro aplikaci Finance and Operations. Použijte místní účet, který je zobrazen v poli LCS.
5. Otevřete prohlížeč událostí.
6. Vyberte **Protokoly aplikací a služeb \> Microsoft \> Dynamics \> AX -DualWriteSync \> Provozní**.
7. Prohlédněte si seznam posledních chyb.

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a>Zrušte propojení a propjte jiné prostředí Dataverse z aplikace Finance and Operations

**Požadovaná role pro zrušení propojení prostředí:** Správce systému buď pro aplikaci Finance and Operations nebo Dataverse.

1. Přihlášení do aplikace Finance and Operations.
2. Přejděte na **Pracovní prostory \> Správa dat** a vyberte dlaždici **Dvojí zápis**.
3. Vyberte všechna spuštěná mapování a pak vyberte **Zastavit**.
4. Zvolte **Odpojit prostředí**.
5. Vyberte **Ano**, chcete-li potvrdit operaci.

Nyní můžete propojit nové prostředí.

## <a name="unable-to-view-the-sales-order-line-information-form"></a>Nelze zobrazit formulář informací o řádku prodejní objednávky 

Po vytvoření prodejní objednávky v produktu Dynamics 365 Sales se můžete kliknutím na možnost **+ Přidat produkty** přesměrovat do formuláře řádku objednávky Dynamics 365 Project Operations. Neexistuje žádný způsob, jak z tohoto formuláře zobrazit formulář **Informace** pro řádek prodejní objednávky. Možnost pro **informace** není zobrazena v rozevírací nabídce pod položkou **Nový řádek objednávky**. K tomu dojde, protože operace projektu byly nainstalovány ve vašem prostředí.

Chcete-li znovu povolit možnost formuláře **Informace**, postupujte následujícím způsobem:
1. Přejděte na entitu **Řádek** tabulky.
2. Vyhledejte formulář **Informace** v uzlu formulářů. 
3. Vyberte formulář **Informace** a klikněte na možnost **Povolit role zabezpečení**. 
4. Změňte nastavení zabezpečení na **Zobrazit všem**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]