---
title: Spouštění vlastních skriptů X++ s nulovými prostoji
description: Toto téma popisuje, jak nahrát a spustit nasaditelné balíčky, které obsahují vlastní skripty X++, aniž byste museli pozastavit váš systém.
author: AndersGirke
ms.date: 12/16/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-12-16
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: fcd0a472fa5116ca0b3a59561b6eeb72181a9113
ms.sourcegitcommit: 44e6875e974a3a1b3e1d7a24c1a3cff3d3697cdc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2022
ms.locfileid: "8088337"
---
# <a name="run-custom-x-scripts-with-zero-downtime"></a>Spouštění vlastních skriptů X++ s nulovými prostoji

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Tato funkce vám umožňuje nahrávat a spouštět nasaditelné balíčky, které obsahují vlastní skripty X++, aniž byste museli využívat služby Microsoft Dynamics Lifecycle Services (LCS) nebo pozastavit systém. Proto můžete opravit drobné nekonzistence dat, aniž by to způsobilo rušivé prostoje.

Výhodou použití skriptu X++ k opravě drobných nekonzistencí dat je fakt, že systém při spuštění skriptu automaticky upraví všechny související tabulky podle potřeby. Tento přístup pomáhá zajistit integritu opravy a pomáhá minimalizovat riziko zavedení nových nesrovnalostí.

> [!IMPORTANT]
> Tato funkce je určena pouze pro opravu drobných nekonzistencí dat. Nesmí se používat pro následující účely ani pro žádný jiný účel:
>
> - Shromažďování dat
> - Změny schémat
> - Migrace dat nebo jiné dlouhotrvající procesy
> - Oprava dat, které lze opravit jinými prostředky, jako jsou běžné obchodní procesy, nástroje konzistence dat nebo jiné samoobslužné nástroje
>
> Tato funkce umožňuje oprávněným uživatelům měnit entity a jejich záznamy přímo, aniž by museli spouštět obchodní logiku, která je s těmito entitami spojena. Tyto změny mohou způsobit problémy s integritou dat. Vaše organizace proto může vyžadovat, abyste před a/nebo po spuštění skriptu získali souhlas od interních a externích auditorů (nebo jiných ekvivalentních zainteresovaných stran). Z důvodu dodržování předpisů mohou být změny, které ovlivňují některé charakteristiky, také zveřejněny v externích zprávách (jako jsou účetní závěrky) nebo oznámeny vládním úřadům. Vaše organizace je výhradně odpovědná za jakékoli změny provedené v jejích datech prostřednictvím této funkce, za jakékoli schválení nebo zveřejnění těchto změn a za dodržování platných zákonů. Veškerá rizika používání této funkce nesete vy.

Všechny nasaditelné balíčky, které jsou nahrány do systému, procházejí povinným pracovním postupem. Z bezpečnostních důvodů a za účelem zajištění oddělení povinností nemá uživatel, který nahraje rozmístitelný balíček, povoleno jej schválit pro další kroky v pracovním postupu. Musí to schválit jiný uživatel. Po schválení balíčku však uživatel, který jej nahrál, bude moci dokončit zbývající kroky.

Systém vyžaduje, aby všechny nasaditelné balíčky prošly testovacím provozem. Než bude skriptu povoleno běžet na produkčních datech, musí uživatel ověřit správnost výstupu výběrem možnosti **Schválit protokol testu**. Pokud výstup není správný, musí uživatel označit balíček jako neúspěšný výběrem možnosti **Opustit**. V tomto případě nebude možné skript spustit na produkčních datech.

Každý nahraný balíček je uložen v systému a prochází definovaným pracovním postupem událostí. U každé události systém uchovává protokol, který obsahuje časové razítko a identitu osoby, která událost provedla. Tímto způsobem systém zajišťuje existenci auditní stopy.

Jak ukazuje následující obrázek, systém poskytuje podrobnosti o tom, jak byly jednotlivé nasaditelné balíčky spuštěny v X++ a které entity byly dotčeny.

![Stránka Podrobnosti skriptu.](media/script-details.png "Stránka Podrobnosti skriptu")

## <a name="assign-duties-to-users-to-control-access"></a>Přidělení povinností uživatelů k řízení přístupu

Tato funkce poskytuje následující povinnosti. Správci mohou tyto povinnosti využít ke kontrole přístupu k této funkci.

- **Udržovat vlastní skripty** – Tato povinnost poskytuje možnost nahrávat, testovat, ověřovat a spouštět vlastní skripty X++ v prostředích (testování přijetí uživatelem \[UAT\] a výroba).
- **Schválit vlastní skripty** – Tato povinnost poskytuje možnost schvalovat nahraný vlastní skript X++. Schválení je povinným krokem předtím, než bude možné otestovat, ověřit a spustit jakýkoli skript.

Aby se minimalizovalo riziko škodlivé akce, musí být každý skript výslovně schválen jiným uživatelem, než je uživatel, který jej nahrál. Než budete moci tuto funkci ve své organizaci používat, musí správce přidělit předchozí povinnosti alespoň dvěma relevantním a vysoce důvěryhodným uživatelům. Ačkoli jeden uživatel může mít obě povinnosti, tento uživatel stále nebude moci schvalovat své vlastní skripty.

## <a name="create-a-deployable-package"></a>Vytvoření nasaditelného balíčku

Tato funkce vyžaduje běžný nasaditelný balíček, který lze vytvořit v aplikaci Visual Studio. Pokyny naleznete v tématu [Vytvoření nasaditelných balíčků modelů](../deployment/create-apply-deployable-package.md).

Váš nasaditelný balíček musí obsahovat přesně jednu spustitelnou třídu X++. Jinými slovy, musí mít jednu třídu obsahující metodu, která má následující podpis.

```xpp
public static void main(Args _args)
```

> [!NOTE]
> Název hlavní metody musí být psán malými písmeny.

## <a name="code-example"></a>Příklad kódu

Následující příklad kódu ukazuje, jak lze strukturovat nasaditelný balíček.

```xpp
class MyScriptClassForIssueXYZ
{
    public static void main(Args _args)
    {
        if (curExt() != 'DAT')
        {
            throw error("This script must run in the DAT company!");
        }

        ttsbegin;

        MyTable myTable;

        update_recordset myTable
            setting myField = 17
            where myTable.myReference == 'xyz';

        if (myTable.RowCount() != 1)
        {
            throw error("Not updating the expected row!");
        }

        info("Success");
  
        ttscommit;
    }

}
```

## <a name="best-practices"></a>Doporučené postupy

Následující seznam popisuje některé osvědčené postupy pro úspěšné psaní, implementaci a spuštění skriptu. Seznam není vyčerpávající a měl by být považován pouze za vodítko.

- Na konci skriptu **vypište** zprávu o úspěchu. Tímto způsobem dáte najevo, že skript běžel bez výjimek.
- **Přidejte** explicitní zpracování rozsahu transakce.
- **Využijte** existující obchodní logiku, jako např. metody `update()`, ale **neobcházejte** obchodní logiku pomocí metod `doUpdate()`, `doInsert()` a `doDelete()`. Tento přístup pomůže zajistit správné zpracování závislých dat. Výrazně také sníží riziko dalších nekonzistencí dat.
- **Uplatňujte** kontext společnosti. Tento přístup odhalí běžné chyby při běhu skriptu. Například odhalí, zda skript není spuštěn ve špatné společnosti.
- **Trvejte** na tom, aby počet dotčených záznamů odpovídal vašim očekáváním. Tento přístup odhalí, zda se data neočekávaně neposunula v systému během přípravy skriptu.
- **Používejte** jedinečné názvy tříd pro každý skript (například zahrnutím odkazu na pracovní položku do názvu). Tento přístup zabrání kolizím názvů při nahrávání skriptu. Pokud je vyžadována nová iterace skriptu, nezapomeňte ji dát nový název.
- **Testujte** každý skript nejprve v neprodukčním prostředí. Otestujte zamýšlený dopad a neúmyslné vedlejší účinky na související údaje. Zajistěte, aby všechny obchodní procesy, které by mohly být ovlivněny, mohly být poté úspěšně a plně dokončeny.

## <a name="upload-and-run-a-deployable-package"></a>Nahrajte a spusťte nasaditelný balíček

Pomocí následujícího postupu nahrajete a spustíte skript.

1. Ve finanční a provozní aplikaci přejděte na nabídku **Správa systému \> Periodické úkoly \> Databáze \> Vlastní skripty**.
1. Vyberte **Odeslat**.
1. Vyberte nasaditelný balíček, který jste vytvořili, jak je popsáno dříve v tomto tématu. Budete vyzváni k zadání účelu skriptu.
1. Skript nyní musí schválit jiný uživatel než ten, který jej nahrál. Schvalovatel musí postupovat takto:

    1. Přejděte do nabídky **Správa systému \> Periodické \> Databáze \> Vlastní skripty**.
    1. Vyberte skript, který chcete schválit, a poté vyberte **Podrobnosti**.
    1. V podokně akcí na kartě **Pracovní postup procesu** ve skupině **Spustit** zvolte **Schválit** nebo **Zamítnout**. Pokud vyberete **Schválit**, skript je označen jako schválený a je odemčen pro testování. Pokud vyberete **Zamítnout**, skript je uzamčen. V obou případech je událost zaprotokolována a kopie skriptu je uchovávána v systému.

1. Skript musí být otestován, aby bylo zajištěno, že dělá to, k čemu je určen. Tester může být stejný jako uživatel, který nahrál video nebo schvalovatel, nebo to může být třetí uživatel, který má požadovaná oprávnění. Tester musí postupovat takto:

    1. Přejděte do nabídky **Správa systému \> Periodické \> Databáze \> Vlastní skripty**.
    1. Vyberte skript, který chcete otestovat, a poté vyberte **Podrobnosti**.
    1. V podokně akcí na kartě **Pracovní postup procesu** ve skupině **Test** zvolte **Spustit test**. Skript se spouští uvnitř dočasné transakce, kterou systém automaticky přeruší, zatímco shromažďuje různé protokoly a příkazy SQL.
    1. Po dokončení skriptu zkontrolujte protokoly a ověřte, zda výsledky splňují vaše očekávání. Proveďte jeden z následujících kroků:

        - Pokud jste s výsledkem testu spokojeni, vyberte možnost **Schválit protokol testu** ve skupině **Test** na kartě **Pracovní postup procesu** v podokně akcí, abyste umožnili spuštění skriptu. Protokol událostí bude odrážet skutečnost, že byl skript testován, a bude uvádět, kdo a kdy jej testoval.
        - Pokud nejste s výsledkem testu spokojeni, vyberte možnost **Opustit** ve skupině **Konec** na kartě **Pracovní postup procesu** v podokně akcí, abyste zabránili spuštění skriptu. Systém bude uchovávat kopii skriptu spolu s protokolem jeho historie.

1. Až si budete jisti, že skript splňuje vaše očekávání, vyberte **Spustit** ve sklupině **Spustit** na kartě **Pracovní postup procesu** v podokně akcí as spusťte ho. Tento příkaz provede totéž jako předchozí testovací běh, ale transakce bude na konci potvrzena.
1. Po dokončení běhu skriptu zkontrolujte výsledek a potvrďte, že skript fungoval tak, jak jste zamýšleli. Proveďte jeden z následujících kroků:

    - Pokud jste s výsledkem spokojeni, vyberte možnost **Účel vyřešen** ve skupině **Konec** na kartě **Pracovní postup procesu** v podokně akcí. Protokol událostí bude odrážet skutečnost, že skript byl úspěšně spuštěn, a bude uvádět, kdo a kdy jej ověřil. Skript je uložen, ale nyní je uzamčen a nelze jej znovu spustit.
    - Pokud nejste s výsledkem spokojeni, vyberte možnost **Účel nevyřešen** ve skupině **Konec** na kartě **Pracovní postup procesu** v podokně akcí. Protokol událostí bude odrážet skutečnost, že skript nebyl úspěšně spuštěn, a bude uvádět, kdo a kdy jej spustil. Skript je uložen, ale nyní je uzamčen a nelze jej znovu spustit. Systém však akci skriptu automaticky nevrátí. Možná budete muset napsat, importovat a spustit nový skript, abyste zrušili dopad neúspěšného skriptu na váš systém.

Váš výběr v posledním kroku definuje konečný stav skriptu. Proces můžete opakovat podle potřeby.

## <a name="upload-and-run-a-deployable-package-through-lcs"></a>Nahrajte a spusťte nasaditelný balíček prostřednictvím LCS

Namísto nasazení balíčku prostřednictvím uživatelského rozhraní finanční a provozní aplikace, jak je popsáno v předchozí části, jej můžete nahrát do LCS a použít běžný postup k jeho nasazení. Více informací najdete v tématu [Instalace nasaditelných balíčků z příkazového řádku](../deployment/install-deployable-package.md).

Ačkoli má tento přístup méně omezení, poskytuje menší ochranu proti chybám. Navíc, protože to vyžaduje restart všech serverů, způsobí to určitý výpadek.
