---
title: Pořadí údržby
description: Toto téma popisuje pořadí údržby v modulu Správa majetku.
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRoundTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: dc0d8ec546e7455187a87ac124c5e56a93f5bafd2270bf275af950991fc4b87e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740712"
---
# <a name="maintenance-rounds"></a>Pořadí údržby

[!include [banner](../../includes/banner.md)]

 

V modulu **Správa majetku** můžete vytvořit pořadí údržby pro různé položky majetku, u kterých je třeba v pravidelných intervalech provádět podobné úkoly. Například úlohy namazání nebo úlohy bezpečnostní prohlídky, které je třeba provést na několika strojích ve stejných intervalech. Prvním krokem je vytvoření pořadí údržby, včetně majetku, který vyžaduje stejný formulář práce údržby. Dále naplánujete pořadí údržby. Po vytvoření rozvrhu pořadí údržby můžete zobrazit všechny záznamy úloh, které se týkají pořadí, v částech **Všechny rozvrhy údržby** a **Otevřené řádky rozvrhu údržby**.

>[!NOTE]
>Pořadí úržby lze vytvořit i ve funkčních místech pro dokončení pro položky majetku instalované ve funkčních místech v čase vytvoření pracovního příkazu na základě pořadí. Další informace o nastavení pořadí údržby pro funkční místa naleznete v tématu [Vytvoření funkčních míst](../functional-locations/create-functional-locations.md).

## <a name="set-up-a-maintenance-round"></a>Nastavení pořadí údržby

1. Klikněte na **Správa majetku** > **Nastavení** > **Preventivní údržba** > **Pořadí údržby**.

2. Nové pořadí údržby vytvoříte klepnutím na položku **Nový**.

3. Do pole **Pořadí údržby** zadejte ID a do pole **Název** zadejte název pořadí údržby.

4. V poli **Počáteční datum** vyberte počáteční datum pořadí.

5. Do polí **Dokončit v řádu dnů** a **Dokončit v řádu hodin** můžete zadat očekávané koncové datum ve dnech nebo hodinách. Očekávané koncové datum je vypočítáno relativně k datu zahájení, které je vypočítáno při vytvoření řádků rozvrhu údržby. Chcete-li například určit, že související úloha má být dokončena do týdne od počátečního data, můžete do pole **Dokončit v řádu dnů** vložit hodnotu „7“.

6. Chcete-li automaticky vytvořit pracovní příkazy z řádků rozvrhu údržby vytvořených z tohoto pořadí údržby, vyberte možnost „Ano“ na přepínači **Automaticky vytvořit**.

7. V poli **Typ pracovního příkazu** vyberte typ pracovního příkazu, který se použije pro pracovní příkazy vytvořené z tohoto pořadí údržby.

8. V poli **Úroveň služeb** vyberte úroveň služeb pracovního příkazu, který se použije pro pracovní příkazy vytvořené z tohoto pořadí údržby.

9. Na záložce s náhledem **Řádky majetku** kliknutím na **Přidat** přidáte majetek do plánu údržby.

10. Číslo řádku se automaticky vloží do pole **Číslo řádku** a označuje posloupnost položek majetku v pořadí údržby.

11. V poli **Majetek** vyberte majetek.

12. V poli **Typ práce údržby** vyberte typ práce údržby pro majetek.

13. V případě potřeby vyberte **Vyrianta typu práce údržby** a **Obor** související s typem práce údržby.

14. Vyberte opakování (den, týden atd.) v poli **Typ období**.

15. Do pole **Frekvence období** zadejte počet opakování pro plán údržby. Příklad: Pokud jste v poli **Typ období** vybrali možnost „Den“ a do tohoto pole zadáte číslo „7“, budou během plánování preventivní údržby jednou týdně vytvořeny nové řádky pořadí údržby.

16. V poli **Počáteční datum** vyberte počáteční datum majetku, který má být součástí pořadí údržby. Toto datum se může lišit od počátečního data pořadí údržby.

17. Chcete-li přidat více položek majetku do pořadí údržby, zopakujte kroky 9 až 16.

18. Na záložce s náhledem **Řádky funkčních míst** kliknutím na **Přidat** přidáte funkční místo do plánu údržby. Viz popis souvisejících polí výše. Stejná pole jsou k dispozici jako pro vytvoření řádku majetku, ale v případě potřeby můžete také vybrat možnost **Výrobce** a **Model** pro funkční místo. Pokud jste vybrali pouze funkční místo na řádku, ale nevytvoříte žádný výběr pro **Typ majetku**, **Výrobce**, **Model**, **Typ práce údržby**, **Varianta typu práce údržby** a **Obor**, veškerý majetek související s tímto funkčním místem v době plánování údržby bude zahrnut do pořadí údržby.

19. Na záložce s náhledem **Fondy** klikněte na tlačítko **Přidat** a vyberte fond pracovních příkazů, který má být zahrnut do pořadí údržby. K jednomu pořadí údržby lze připojit několik fondů pracovních příkazů.

20. Uložte provedené nastavení.

>[!NOTE]
>Pole **Majetek** a **Řádky** umístěné ve skupině **Podrobnosti** na záložce s náhledem **Záhlaví** zobrazují celkový počet položek majetku a řádků souvisejících s vybraným pořadím údržby.

Následující obrázek znázorňuje ukázku a příklad pořadí údržby obsahující tři aktiva.

![Obrázek č. 1.](media/13-preventive-maintenance.png)


## <a name="schedule-maintenance-rounds"></a>Naplánovat pořadí údržby

Když nastavíte pořadí údržby, spusťte úlohu plánu, která plánuje všechny úlohy související s pořadím údržby.

1. Klikněte na **Správa majetku** > **Pravidelně** > **Preventivní údržba** > **Rozvrhnout pořadí údržby** nebo **Správa majetku** > **Společné** > **Rozvrh údržby** > **Všechny rozvrhy údržby** nebo **Otevřené řádky rozvrhu údržby** nebo **Otevřené fondy rozvrhu údržby** > v seznamu vyberte řádek rozvrhu údržby > tlačítko **Plány údržby**.

2. V poli **Období** vyberte typ období, které se má použít pro úlohu plánování.

3. V poli **Frekvence období** zadejte počet období, která mají být zahrnuta do úlohy plánování. Zahájení plánování je aktuální datum.

4. Chcete-li, aby byla na základě plánu údržby zaokrouhlení automaticky vytvořen pracovní příkaz, vyberte možnost „Ano“ na přepínači **Automaticky vytvořit**.

>[!NOTE]
>Je-li toto přepínací tlačítko nastaveno na hodnotu „Ano“ a přepínač **Automaticky vytvořit** je nastaven na „Ano“ pro plán údržby ve formuláři **Pořadí údržby**, budou vytvořeny pracovní příkazy na základě řádků pořadí údržby a budou vytvořeny také řádky plánu údržby se stavem „Pracovní příkaz vytvořen“. Je-li v tomto rozevíracím seznamu nebo ve formuláři **Pořadí údržby** nastaveno pouze jedno z přepínacích tlačítek **Automaticky vytvořit**, budou vytvořeny pouze řádky rozvrhu údržby ve stavu „Vytvořeno“. V takovém případě se žádné pracovní příkazy nevytvoří.

5. Je-li to nutné, můžete vybrat konkrétní pořadí nebo jiné počáteční datum pro úlohu plánu. Klikněte namožnost **Filtr** a přidejte pořadí.

6. Klikněte na tlačítko **OK**.

7. Nyní můete zobrazit úlohy pořadí údržby v částech **Správa majetku** > **Společné** > **Rozvrh údržby** > **Všechny rozvrhy údržby** nebo **Otevřené řádky rozvrhu údržby**. Jsou-li pořadí údržby připojena k fondu pracovních příkazů, zobrazí se také řádky rozrvhu údržby v části **Otevřené fondy rozvrhu údržby**. Řádky rozvrhu údržby vytvořené z pořadí mají typ odkazu „Rozvrhy údržby“.

Následující dvě ilustrace zobrazují **úlohu plánování v** dialogovém okně Naplánovat pořadí údržby a řádky plánu údržby vytvořené ve **všech plánech** údržby na základě této úlohy plánu.

![Obrázek č. 2.](media/14-preventive-maintenance.png)

![Obrázek č. 3.](media/15-preventive-maintenance.png)

- Pokud jsou pro majetek, na který se vztahuje záruka dodavatele, vytvořeny pracovní příkazy ručně, zobrazí se dialogové okno, které uživatele upozorní na záruku. Vytvoření pracovního příkazu lze v tuto chvíli zrušit. Kontrola vztahu záruky je vynechána pro automaticky vytvořené pracovní příkazy.  
- Na záložce s náhledem **Spustit na pozadí** můžete nastavit dávkovou úlohu pro plánování pořadí v pravidelných intervalech.  
- Pokud je v několika fondech pracovních příkazů uvedeno pořadí (viz [Fondy pracovních příkazů](../work-orders/work-order-pools.md)), zobrazí se jeden záznam pro každý fond v části **Otevřené fondy rozvrhu údržby**. To je provedeno za účelem optimalizace možností filtrování pro fondy pracovních příkazů.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]