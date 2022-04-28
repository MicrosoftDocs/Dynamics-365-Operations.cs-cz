---
title: Obecné řešení potíží
description: Toto téma obsahuje obecné informace o odstraňování potíží pro integrací dvojitého zápisu mezi aplikacemi Finance a Operace a Dataverse.
author: RamaKrishnamoorthy
ms.date: 04/07/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 8b5951f9f40179ca0bf31f5cccf1f05a0f968213
ms.sourcegitcommit: 1843235766b6f8cf950a13a310e9f4f2f53c59a4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/07/2022
ms.locfileid: "8554592"
---
# <a name="general-troubleshooting"></a>Obecné řešení potíží

[!include [banner](../../includes/banner.md)]



Toto téma obsahuje obecné informace o odstraňování potíží pro integrací dvojitého zápisu mezi aplikacemi Finance a Operace a Dataverse.

> [!IMPORTANT]
> Některé problémy, které toto téma řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD). Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Chcete-li zobrazit podrobnosti chyby, povolte a zobrazte protokol sledování modulů plug-in v Dataverse

Protokoly trasování mohou být užitečné při řešení problémů se živou synchronizací s duálním zápisem mezi Finance a Operations a Dataverse. Protokoly mohou poskytnout konkrétní podrobnosti týmům, které poskytují technickou a technickou podporu pro Dynamics 365. Tento článek popisuje, jak povolit protokoly trasování a jak je zobrazit. Protokoly trasování se spravují na stránce Nastavení Dynamics 365 a ke změně a zobrazení vyžadují oprávnění na úrovni správce. 

**Požadovaná role pro zapnutí protokolu sledování a zobrazení chyb:** správce systému

### <a name="turn-on-the-trace-log"></a>Zapněte protokol trasování
Chcete-li zapnout protokol sledování, postupujte následujícím způsobem.

1.  Přihlaste se k Dynamics 365 a pak na horním navigačním panelu vyberte **Nastavení**. Na stránce Systémy klikněte na **Správa**.
2.  Na stránce Správa zvolte **Nastavení systému**.
3.  Vyberte kartu **Vlastní nastavení** a plug-in a pak v sekci vlastní sledování aktivity workflowu změňte rozevírací nabídku na **Všechny**. To bude sledovat všechny aktivity a poskytne komplexní soubor dat pro týmy, které musí prověřit potenciální problémy.

> [!NOTE]
> Nastavení rozevíracího seznamu na **Výjimka** poskytne informace o sledování pouze v případě, že dojde k výjimkám (chybám).

Po povolení budou protokoly trasování zásuvného modulu nadále shromažďovány, dokud je ručně nevypnete návratem do tohoto umístění a výběrem **Vypnuto**.

### <a name="view-the-trace-log"></a>Zobrazení protokolu trasování
Chcete-li zobrazit protokol sledování, postupujte následujícím způsobem.

1. Na stránce Nastavení Dynamics 365 na horním navigačním panelu vyberte **Nastavení**. 
2. Vyberte **Protokol trasování pluginu** v sekci **Přizpůsobení** stránky.
3. Položky můžete najít v seznamu protokolů trasování na základě názvu typu a/nebo názvu zprávy.
4. Chcete-li zobrazit celý protokol, otevřete požadovaný záznam. Blok zpráv v sekci Provedení poskytne dostupné informace o zásuvném modulu. Pokud jsou k dispozici, budou poskytnuty také podrobnosti o výjimce. 

Můžete zkopírovat obsah protokolů trasování a vložit je do jiné aplikace, jako je Poznámkový blok nebo jiné nástroje, abyste mohli zobrazit protokoly nebo textové soubory, abyste snadněji viděli veškerý obsah. 

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Povolit režim ladění pro řešení potíží se živými synchronizacemi v finančních a provozních aplikacích

**Požadovaná role pro zobrazení chyb:** správce systému

Chyby dvojího zapisování, které pocházejí z aplikace Dataverse, se mohou objevit ve finanční a provozní aplikaci. Pomocí následujících kroků můžete zapnout podrobné protokolování chyb:

1. Všechny konfigurace projektu ve finanční a provozní aplikaci mají příznak **IsDebugMode** v tabulce **DualWriteProjectConfiguration**.
2. Otevřete **DualWriteProjectConfiguration** pomocí doplňku aplikace Excel. Chcete-li doplněk použít, povolte režim návrhu v doplňku Finance a Operace pro Excel a přidejte **DualWriteProjectConfiguration** na list. Další informace viz [Zobrazit a aktualizovat data entit pomocí Excelu](../../office-integration/use-excel-add-in.md).
3. Nastavte **IsDebugMode** na **Ano** v projektu.
4. Spuštění scénáře generujících chyby.
5. Podrobné protokoly jsou uloženy v tabulce **DualWriteErrorLog**.
6. Chcete-li vyhledat data v prohlížeči tabulky, použijte následující odkaz: `https://999aos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog` nahraďte `999` podle potřeby.
7. Aktualizujte znovu po [KB 4595434](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=98e5dc124ac125c57ad633d885ac612aea3ddb8f4abf9d71ab3aa354f2e06cbe), který je k dispozici pro aktualizace platformy 37 a novější. Pokud máte tuto opravu nainstalovanou, režim ladění zachytí více protokolů.  

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Zkontrolujte chyby synchronizace ve virtuálním počítači pro finanční a provozní aplikaci

**Požadovaná role pro zobrazení chyb:** Správce systému

1. Přihlaste se do Microsoft Dynamics Lifecycle Services (LCS).
2. Otevřete projekt LCS, který jste zvolili pro testování dvojího zápisu.
3. Zvolte dlaždici **Prostředí hostovaná v cloudu**.
4. Pomocí vzdálené plochy se přihlaste k virtuálnímu počítači (VM) pro finanční a provozní aplikaci. Použijte místní účet, který je zobrazen v poli LCS.
5. Otevřete prohlížeč událostí.
6. Vyberte **Protokoly aplikací a služeb \> Microsoft \> Dynamics \> AX -DualWriteSync \> Provozní**.
7. Prohlédněte si seznam posledních chyb.

## <a name="dual-write-ui-landing-page-showing-blank"></a>Vstupní stránka s duálním zápisem uživatelského rozhraní je prázdná
Při otevření stránky s duálním zápisem v prohlížeči Microsoft Edge nebo Google Chrome se domovská stránka nenačte a zobrazí se prázdná stránka nebo chyba, jako je „Něco se pokazilo“.
V Devtools se v protokolech konzoly zobrazuje chyba:

>bundle.eed39124e62c58ef34d2.js:37 DOMException: Nepodařilo se načíst vlastnost 'sessionStorage' z 'Window': Přístup je pro tento dokument zamítnut. at t.storeInSessionStorage (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:16:136860 ) at new t (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:69:20103 ) at ci (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:44115 ) at Eo (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:58728 ) at jo (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:65191 ) at Nr (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:84692 ) at Or (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:85076 ) at Ss (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:91750 ) at vs (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:91130 ) at hs (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:90151 )

Uživatelské rozhraní používá „úložiště relace“ prohlížeče k uložení některých hodnot vlastností pro načtení domovské stránky. Aby to fungovalo, musí být v prohlížeči webu povoleny soubory cookie třetích stran. Chyba naznačuje, že uživatelské rozhraní nemá přístup k úložišti relace. K tomuto problému mohou nastat dva scénáře:

1.  Otevíráte uživatelské rozhraní v anonymním režimu Edge/Chrome a soubory cookie třetích stran v anonymním režimu jsou blokovány.
2.  V Edge/Chrome jste zcela zablokovali soubory cookie třetích stran.

### <a name="mitigation"></a>Zmírnění dopadů
V nastavení prohlížeče musí být povoleny soubory cookie třetích stran.

### <a name="google-chrome-browser"></a>Prohlížeč Google Chrome
1. možnost:
1.  Přejděte do nastavení zadáním chrome://settings/ do adresního řádku a poté přejděte na Soukromí a zabezpečení -> Soubory cookie a další data webu.
2.  Vyberte 'Povolit všechny soubory cookie'. Pokud si to nepřejete, přejděte na druhou možnost.

2. možnost:
1.  Přejděte do nastavení zadáním chrome://settings/ do adresního řádku a poté přejděte na Soukromí a zabezpečení -> Soubory cookie a další data webu.
2.  Pokud je vybrána možnost „Blokovat soubory cookie třetích stran v anonymním režimu“ nebo „Blokovat soubory cookie třetích stran“, přejděte na „Weby, které mohou vždy používat soubory cookie“ a klikněte na **Přidat**. 
3.  Přidejte název webu aplikací Finance & Operations – https://<your_FinOp_instance>.cloudax.dynamics.com. Ujistěte se, že jste zaškrtli políčko „Všechny soubory cookie, pouze na tomto webu“. 

### <a name="microsoft-edge-browser"></a>Prohlížeč Microsoft Edge
1.  Přejděte do Nastavení -> Oprávnění webu -> Soubory cookie a data webu.
2.  Vypněte možnost „Blokovat soubory cookie třetích stran“.  

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a>Odpojení a propojení jiného prostředí Dataverse z finanční a provozní aplikace

**Požadovaná role pro zrušení propojení prostředí**: Správce systému buď pro finanční a provozní aplikaci nebo Dataverse.

1. Přihlášení do finanční a provozní aplikace.
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

### <a name="google-chrome-browser"></a>Prohlížeč Google Chrome

1. Na otevřené kartě stiskněte **F12** nebo vyberte **Vývojářské nástroje** a otevřete nástroje pro vývojáře.
2. Otevřete kartu **Síť** a zadejte **integ** v textovém poli filtru.
3. Spusťte svůj scénář a sledujte protokolované požadavky.
4. Klikněte pravým tlačítkem na položky a vyberte **Uložit vše jako HAR s obsahem**.

### <a name="microsoft-edge-browser"></a>Prohlížeč Microsoft Edge

1. Na otevřené kartě stiskněte **F12** nebo vyberte **Vývojářské nástroje** a otevřete nástroje pro vývojáře.
2. Otevřete kartu **Síť**.
3. Spusťte svůj scénář.
4. Vyberte **Uložit**, chcete-li exportovat výsledky jako HAR.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
