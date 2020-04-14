---
title: Obecné řešení potíží
description: Toto téma obsahuje všeobecné informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f7ee0b5aa4e72614205e129acd986376b33efc70
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172684"
---
# <a name="general-troubleshooting"></a>Obecné řešení potíží

[!include [banner](../../includes/banner.md)]



Toto téma obsahuje všeobecné informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Common Data Service.

> [!IMPORTANT]
> Některé problémy, které toto téma řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD). Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a>Při pokusu o instalaci balíčku dvojího zapisování pomocí nástroje package deployer se nezobrazí žádná dostupná řešení

Některé verze nástroje package deployer nejsou kompatibilní s balíčkem řešení dvojího zápisu. Chcete-li úspěšně nainstalovat balíček, je nutné použít [verzi 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) nebo novější z nástroje package deployer.

Po instalaci nástroje package deployer nainstalujte balíček řešení pomocí následujících kroků.

1. Stáhněte si nejnovější soubor balíčku řešení z Yammer.com. Po stažení souboru ZIP balíčku klepněte na něj pravým tlačítkem myši a vyberte **Vlastnosti**. Zaškrtněte políčko **odblokovat** a vyberte **Použít**. Není-li zaškrtávací políčko **Odblokovat** zobrazeno, je již zrušeno blokování souboru zip a tento krok můžete přeskočit.

    ![Dialogové okno Vlastnosti](media/unblock_option.png)

2. Extrahujte soubor zip balíčku a zkopírujte všechny soubory ve složce **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438.**

    ![Obsah složky Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438](media/extract_package.png)

3. Vložte všechny zkopírované soubory do složky **Nástroje** v nástroji Package Deployer. 
4. Spuštěním **PackageDeployer.exe** vyberte prostředí Common Data Service a nainstalujte řešení.

    ![Obsah složky Nástroje](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details"></a>Chcete-li zobrazit podrobnosti chyby, povolte a zobrazte protokol sledování modulů plug-in v Common Data Service

**Požadovaná role pro zapnutí protokolu sledování a zobrazení chyb:** správce systému

Chcete-li zapnout protokol sledování, postupujte následujícím způsobem.

1. Přihlaste se k aplikaci Finance and Operations, otevřete stránku **Nastavení** a v části **Systém** vyberte možnost **Správa**.
2. Na stránce **Správa** zvolte **Nastavení systému**.
3. Na kartě **Vlastní nastavení** v poli **Modul plug-in a vlastní sledování aktivity workflowu** vyberte možnost **Vše**, chcete-li povolit trasovací protokol modulu plug-in. Chcete-li protokolovat protokoly trasování pouze při výskytu výjimek, můžete namísto toho vybrat **Výjika**.


Chcete-li zobrazit protokol sledování, postupujte následujícím způsobem.

1. Přihlaste se k aplikaci Finance and Operations, otevřete stránku **Nastavení** a v části **vlastní nastavení** vyberte možnost **Protokol sledování modulu plug-in**.
2. Najděte protokoly sledování, kde pole **Název typu** je nastaveno na **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.
3. Chcete-li zobrazit úplný protokol, klikněte dvakrát na položku, a potom na pevné záložce **Spuštění** zkontrolujte text **Message Block**.

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Povolit režim ladění pro řešení potíží se živými synchronizacemi v aplikacích Finance and Operations

**Požadovaná role pro zobrazení chyb:** správce systému

Chyby dvojího zapisování, které pocházejí z aplikace Common Data Service, se mohou objevit v aplikaci Finance and Operations. V některých případech není úplný text chybové zprávy k dispozici, protože zpráva je příliš dlouhá nebo obsahuje osobní identifikační údaje (PII). Pomocí následujících kroků můžete zapnout podrobné protokolování chyb.

1. Všechny konfigurace projektu v aplikacích Finance and Operations mají vlastnost **IsDebugMode** v entitě **DualWriteProjectConfiguration**. Otevřete entitu **DualWriteProjectConfiguration** pomocí doplňku aplikace Excel.

    > [!TIP]
    > Snadným způsobem, jak tuto entitu otevřít, je zapnout režim **Návrh** v doplňku aplikace Excel a poté přidat **DualWriteProjectConfigurationEntity** do listu. další informace získáte v tématu [Otevření dat entity v aplikaci Excel a jejich aktualizace pomocí doplňku aplikace Excel](../../office-integration/use-excel-add-in.md).

2. Nastavte vlastnost **IsDebugMode** na **Ano** pro projekt.
3. Spuštění scénáře generujících chyby.
4. Podrobné protokoly jsou k dispozici v tabulce DualWriteErrorLog. Chcete-li vyhledat data v prohlížeči tabulky, použijte následující adresu URL (nahraďte **XXX**):

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=>DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Zkontrolujte chyby synchronizace ve virtuálním počítači pro aplikaci Finance and Operations

**Požadovaná role pro zobrazení chyb:** správce systému

1. Přihlaste se do Microsoft Dynamics Lifecycle Services (LCS).
2. Otevřete projekt LCS, který jste zvolili pro testování dvojího zápisu.
3. Zvolte dlaždici **Prostředí hostovaná v cloudu**.
4. Pomocí vzdálené plochy se přihlaste k virtuálnímu počítači (VM) pro aplikaci Finance and Operations. Použijte místní účet, který je zobrazen v poli LCS.
5. Otevřete prohlížeč událostí.
6. Vyberte **Protokoly aplikací a služeb \> Microsoft \> Dynamics \> AX -DualWriteSync \> Provozní**.
7. Prohlédněte si seznam posledních chyb.

## <a name="unlink-and-link-another-common-data-service-environment-from-a-finance-and-operations-app"></a>Zrušte propojení a propjte jiné prostředí Common Data Service z aplikace Finance and Operations

**Požadovaná pověření pro zrušení propojení prostředí:** Správa tenanta Azure AD

1. Přihlášení do aplikace Finance and Operations.
2. Přejděte na **Pracovní prostory \> Správa dat** a vyberte dlaždici **Dvojí zápis**.
3. Vyberte všechna spuštěná mapování a pak vyberte **Zastavit**.
4. Zvolte **Odpojit prostředí**.
5. Vyberte **Ano**, chcete-li potvrdit operaci.

Nyní můžete propojit nové prostředí.
