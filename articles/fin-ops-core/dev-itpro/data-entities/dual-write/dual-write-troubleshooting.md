---
title: Obecné řešení potíží
description: Toto téma obsahuje všeobecné informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: b4adc2d83667a05d14a26ace23e5bd8026df4b5f
ms.sourcegitcommit: caa41c076f731f1e02586bc129b9bc15a278d280
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2021
ms.locfileid: "7380205"
---
# <a name="general-troubleshooting"></a>Obecné řešení potíží

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma obsahuje všeobecné informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Dataverse.

> [!IMPORTANT]
> Některé problémy, které toto téma řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD). Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.

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

**Požadovaná role pro zobrazení chyb:** správce systému

Chyby dvojího zapisování, které pocházejí z aplikace Dataverse, se mohou objevit v aplikaci Finance and Operations. Pomocí následujících kroků můžete zapnout podrobné protokolování chyb:

1. Všechny konfigurace projektu v aplikaci Finance and Operations mají příznak **IsDebugMode** v tabulce **DualWriteProjectConfiguration**.
2. Otevřete **DualWriteProjectConfiguration** pomocí doplňku aplikace Excel. Chcete-li doplněk použít, povolte režim návrhu v doplňku Finance and Operations pro Excel a přidejte **DualWriteProjectConfiguration** na list. Další informace viz [Zobrazit a aktualizovat data entit pomocí Excelu](../../office-integration/use-excel-add-in.md).
3. Nastavte **IsDebugMode** na **Ano** v projektu.
4. Spuštění scénáře generujících chyby.
5. Podrobné protokoly jsou uloženy v tabulce **DualWriteErrorLog**.
6. Chcete-li vyhledat data v prohlížeči tabulky, použijte následující odkaz: `https://999aos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog` nahraďte `999` podle potřeby.
7. Aktualizujte znovu po [KB 4595434](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=98e5dc124ac125c57ad633d885ac612aea3ddb8f4abf9d71ab3aa354f2e06cbe), který je k dispozici pro aktualizace platformy 37 a novější. Pokud máte tuto opravu nainstalovanou, režim ladění zachytí více protokolů.  

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

## <a name="how-to-enable-and-save-network-trace-so-that-traces-can-be-attached-to-support-tickets"></a>Jak povolit a uložit trasování sítě, aby bylo možné připojit stopy k podpoře lístků

Tým podpory možná bude muset zkontrolovat trasování sítě, aby vyřešil některé problémy. Chcete-li vytvořit sledování sítě, postupujte následujícím způsobem:

### <a name="chrome"></a>Chrome

1. Na otevřené kartě stiskněte **F12** nebo vyberte **Vývojářské nástroje** a otevřete nástroje pro vývojáře.
2. Otevřete kartu **Síť** a zadejte **integ** v textovém poli filtru.
3. Spusťte svůj scénář a sledujte protokolované požadavky.
4. Klikněte pravým tlačítkem na položky a vyberte **Uložit vše jako HAR s obsahem**.

### <a name="microsoft-edge"></a>Microsoft Edge

1. Na otevřené kartě stiskněte **F12** nebo vyberte **Vývojářské nástroje** a otevřete nástroje pro vývojáře.
2. Otevřete kartu **Síť**.
3. Spusťte svůj scénář.
4. Vyberte **Uložit**, chcete-li exportovat výsledky jako HAR.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
