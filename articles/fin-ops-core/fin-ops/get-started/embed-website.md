---
title: Vložení aplikací třetích stran
description: Toto téma popisuje způsob vložení aplikací třetích stran pro zvýšení funkčnosti produktu.
author: jasongre
ms.date: 08/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, UserWorkspaceAdd, UserWorkspaceConfigureWebsite
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2021-04-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b0471fd2ea9a5e8b07b9e8bc279da53f6a1539ca
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345403"
---
# <a name="embed-third-party-apps"></a>Vložení aplikací třetích stran

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Mnoho zákazníků používá k provozování svého podnikání celou řadu aplikací. Některé z těchto aplikací jsou webové aplikace třetích stran, které fungují ve spojení s aplikacemi Finance and Operations. Chcete-li zajistit plynulejší uživatelské prostředí, můžete použít funkci **Celostránkové aplikace** pro vložení těchto aplikací třetích stran přímo do aplikací Finance and Operations (za předpokladu, že aplikace třetích stran umožňují vložení). Tímto způsobem mohou uživatelé přistupovat k webům a aplikacím, které požadují, aniž by museli přepínat karty nebo okna.

Než budete moci do produktu vložit aplikace třetích stran, musíte zapnout funkci **Celostránkové aplikace** funkce ve Správě funkcí. Potom můžete použít jednu z následujících metod k vložení aplikace nebo webu třetí strany. Tyto metody jsou analogické s metodami, které se používají k vložení aplikací plátna z Microsoft Power Apps do aplikací Finance and Operations.

- Vložte aplikaci nebo web na existující stránku jako stránku nové karty (kontingenční karta, rychlá karta, okno nebo část pracovního prostoru).
- Vytvořte na řídicím panelu nové celostránkové prostředí pro aplikaci nebo web.

## <a name="embed-a-website-on-an-existing-page"></a>Vložení webu na existující stránku

Tento postup použijte, pokud chcete doplnit existující stránku v systému o vloženou aplikaci.

1. Otevřete stránku, kam chcete aplikaci vložit.
2. Otevřete podokno **Přidat aplikaci**:

    1. Vyberte **Nastavení** a poté **Přizpůsobit** k otevření panelu nástrojů **Přizpůsobení**.
    2. Vyberte **Více \> Přidat aplikaci**.

3. Vyberte oblast stránky, kam chcete aplikaci přidat. Tato oblast musí být a *kontejner karty* pro kontingenční kartu, rychlá karta, okno nebo část pracovního prostoru.
4. Vyberte **Web**.
5. Konfigurace vložené aplikace:

    - **Název** – Zadejte text, který by se měl zobrazit pro kartu, která obsahuje vloženou aplikaci. Často budete chtít, aby tento text byl název aplikace.
    - **Adresa URL** – Zadejte umístění aplikace.

    > [!IMPORTANT]
    > - Z bezpečnostních důvodů musí adresa URL používat protokol Hypertext Transfer Protocol Secure (HTTPS).
    > - Aplikace nebo web musí být nakonfigurován tak, aby umožňoval vložení.

6. Vyberte **Uložit** pro vložení aplikace na stránku. Aplikace je přidána jako poslední karta nebo oddíl ve skupině.
7. Potvrďte, že se aplikace zobrazuje podle očekávání. Pokud aplikace není vykreslena, podívejte se na část [Odstraňování problémů](#troubleshooting) dále v tomto tématu.
8. Otevřete volič zobrazení a vyberte **Uložit** (pokud má být aplikace přidružena k aktuálnímu zobrazení) nebo **Uložit jako** (pro uložení aplikace do jiného zobrazení).

    Pokud stránka nemá volič zobrazení (například pokud je stránkou dialogové okno nebo pracovní prostor), můžete tento krok přeskočit.

## <a name="embed-a-website-as-a-full-page-experience-from-the-dashboard"></a>Vložení webu jako celostránkového prostředí z řídicího panelu

Tento postup použijte, pokud aplikace, kterou chcete vložit, nesouvisí s existující stránkou nebo pokud chcete pouze celostránkové prostředí pro aplikaci uvnitř aplikace Finance and Operations.

1. Otevřete řídicí panel.
2. Vyberte a podržte (nebo klikněte pravým tlačítkem) na řídicím panelu, vyberte **Přizpůsobit** a potom vyberte **Přidat stránku**.
3. V podokně **Přidat stránku** Vyberte **Web**.
4. Konfigurace vložené aplikace:

    - **Název** – Zadejte text, který by se měl zobrazit na dlaždici přidané pro vloženou aplikaci na řídicím panelu. Často budete chtít, aby tento text byl název aplikace.
    - **Adresa URL** – Zadejte umístění aplikace.

    > [!IMPORTANT]
    > - Z bezpečnostních důvodů musí adresa URL používat protokol HTTPS.
    > - Aplikace nebo web musí být nakonfigurován tak, aby umožňoval vložení.

5. Vyberte **Uložit** pro přidání aplikace na řídicí panel jako nové dlaždice.
6. Vyberte novou dlaždici na řídicím panelu a potvrďte, že se aplikace zobrazí podle očekávání. Pokud aplikace není vykreslena, podívejte se na část [Odstraňování problémů](#troubleshooting) dále v tomto tématu.

## <a name="sharing-embedded-apps"></a>Sdílení vložených aplikací

Poté, co jste vložili aplikaci pomocí jedné z metod popsaných v předchozích částech, můžete chtít sdílet pohled s ostatními uživateli v systému. Chcete-li sdílet vloženou aplikaci, použijte jednu z následujících metod:

- **Publikovat zobrazení (doporučeno):** Pokud byla vložená aplikace uložena do zobrazení, doporučeným a upřednostňovaným způsobem jejího sdílení je publikování pohledu uživatelům, kteří mají -příslušné role zabezpečení v cílových právnických osobách. V takovém případě uvidí vloženou aplikaci na této stránce pouze požadovaní uživatelé. Další informace o tom, jak zveřejnit zobrazení, viz [Publikování zobrazení](saved-views.md#publishing-views).

    Z řídicího panelu můžete také publikovat aplikaci, která byla vložena jako celostránkové prostředí. Na řídicím panelu vyberte a podržte (nebo klikněte pravým tlačítkem) dlaždici přidruženou k aplikaci, vyberte **Přizpůsobit** a potom vyberte **Publikovat stránku**. Prostředí, které se podobá prostředí *Zobrazení publikování* je zobrazeno a můžete vybrat role zabezpečení, do kterých chcete publikovat. V aktualizaci 10.0.21 nebo novější, pokud je funkce **Vylepšená podpora právnických osob pro uložená zobrazení** zapnutá, můžete aplikaci také publikovat na požadované právnické osoby.

- **Kopírovat přizpůsobení:** Pro stránky, které nepodporují zobrazení (například dialogová okna nebo pracovní prostory), nebo pro celostránkové aplikace můžete zkopírovat přizpůsobení příslušným uživatelům. Další informace viz [Sdílení přizpůsobení](personalize-user-experience.md#sharing-personalizations).

## <a name="viewing-embedded-apps"></a>Zobrazení vložených aplikací

Chcete-li zobrazit vloženou aplikaci na stránce v aplikacích Finance and Operations, otevřete stránku s vloženou aplikací. Nezapomeňte, že na některých stránkách lze k vloženým aplikacím přistupovat pomocí tlačítka **Power Apps** ve standardním podokně akcí. Alternativně se mohou objevit přímo na stránce jako nová karta, záložku s náhledem, okno nebo nový oddíl v pracovním prostoru.

## <a name="editing-or-removing-embedded-apps"></a>Úpravy nebo odebrání vložených aplikací

Po vložení aplikace na stránku možná budete muset upravit její konfiguraci (například změnou štítku sekce nebo adresy URL). Případně jej možná budete muset ze stránky odebrat. Pomocí jednoho z následujících postupů můžete upravit konfiguraci vložené aplikace nebo ji úplně odebrat.

### <a name="apps-that-are-embedded-on-existing-pages"></a>Aplikace vložené na existující stránky

1. Otevřete stránku, kde je aplikace vložená.
2. Vyberte **Nastavení** a poté **Přizpůsobit** k otevření panelu nástrojů **Přizpůsobení**.
3. Vyberte nástroj **Vybrat** a poté vyberte vloženou aplikaci.
4. Chcete-li aplikaci upravit, proveďte požadované změny v její konfiguraci a poté vyberte **Uložit**.

    Chcete-li aplikaci odebrat, vyberte možnost **Odstranit**.

5. Znovu uložte nebo znovu publikujte zobrazení. Všimněte si, že pokud opustíte stránku bez výslovného uložení pohledu, žádná z akcí, které jste provedli v poli **Upravit web** se nezachová.

### <a name="apps-that-are-embedded-from-the-dashboard"></a>Aplikace vložené z řídicího panelu

1. Otevřete řídicí panel.
2. Vyberte a podržte (nebo klikněte pravým tlačítkem) dlaždici přidruženou k vložené aplikaci a vyberte **Přizpůsobit**.
3. Chcete-li aplikaci upravit, vyberte **Upravit stránku**. V podokně **Upravit web** proveďte požadované změny v konfiguraci aplikace a poté vyberte **Uložit**.

    Chcete-li aplikaci odebrat, vyberte možnost **Odstranit stránku**.

## <a name="appendix"></a>Dodatek

### <a name="troubleshooting"></a>Řešení potíží

Pokud se web po vložení do aplikace Finance and Operation nevykreslí správně nebo pokud se zobrazí chybová zpráva s oznámením, že adrese URL bylo odepřeno připojení, je web pravděpodobně nakonfigurován tak, aby zabránil tomu, aby byl vložen do prvku iframe. Podle těchto pokynů zjistíte, zda lze web vložit.

1. Otevřete vývojářské nástroje pro prohlížeč, který používáte.
2. Na kartě **Síť** najděte a vyberte odpověď z vloženého webu.
3. Na kartě **Záhlaví** pod **Záhlaví odpovědí** vyhledejte **x-frame-options**. Pokud **x-frame-options** existuje v záhlavích odpovědí a má hodnotu **DENY** nebo **SAMEORIGIN**, web aktuálně nelze vložit. Abyste mohli bezpečně integrovat aplikaci, budete muset spolupracovat s vlastníkem aplikace.

### <a name="developer-modeling-a-website-on-a-form"></a>[Vývojář] Modelování webu na formuláři

Ačkoli je toto téma zaměřeno na vkládání aplikací nebo webů třetích stran prostřednictvím personalizace, vývojáři je také mohou vložit do formuláře pomocí vývojářského prostředí Visual Studio. Stačí přidat a do formuláře ovládací prvek **WebsiteHostControl**. Vlastnosti metadat, které jsou k dispozici pro ovládací prvek, poskytují stejné možnosti jako prostředí přizpůsobení.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
