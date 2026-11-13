Hermes在Feishu"清一AI hermes多智能群"运行，飞书open_id: ou_1ff0ce1b0457b6eb1e72e2535b3101d0。三省六部9bot在config.yaml platforms.feishu.extra，权限: im:message + im:message:send_as_bot。WeChat DM失败（"No home channel set"是Hermes平台配置问题，非代理）。
§
Obsidian一级目录(实地核对): 0-收件箱/1-在做/2-资料库/3-日记/99-归档+Templates+meta。分析笔记=1-在做/思考/、概念=2-资料库/概念/、人物=2-资料库/人物/、日记=3-日记/00-日记/。meta周日cron自动重写勿手改
§
vision_analyze是stub,看图用computer_use截屏(10-23验证)。cliclick在/opt/homebrew/bin/cliclick。
§
Windows机器：Intel i7-7829X + NVIDIA P2000（独立显卡，CUDA可用）。可用于本地GPU推理（BitNet/llama.cpp等）。jianying-editor-skill已克隆到 ~/.hermes/skills/jianying-editor/（luoluoluo22/jianying-editor-skill，1446⭐，剪映Pro自动化）。自建软件 VideoBitUpscaler（Vibe Coding：低分辨率像素扩散修复→传统放大+8bit→10bit Log转换），夸克分享 pan.quark.cn/s/32132fe3b494，P2000 4GB显存为瓶颈:首选0.2.3 CUDA版,爆显存回退0.2.1/0.2.0;10bit Log需PotPlayer硬解。
§
Nutstore(坚果云) 同步靠菜单栏手动点"立即同步"(无CLI);进程Nutstore/NutstoreFilesD。
§
Nocturne Memory MCP已接入(127.0.0.1:8233/mcp),每日21点cron日记→Nocturne。
§
Tool quirks: patch禁写~/.hermes/config.yaml→execute_code+ruamel; pikepdf覆写需allow_overwriting_input=True; 签名字体优先雨落韵境楷书; computer_use驱动(10-23修复): /Applications/CuaDriver.app(0.28.1)被launchd反复拉起抢socket, 与pin的0.21.0握手失败(契约0.8.0≠0.7.0)→bootout gui/$UID/application.com.trycua.driver.*+kill旧守护+软链~/.local/bin/cua-driver指pinned版。
§
方舟 ARK(火山): OpenAI兼容 base_url ark.cn-beijing.volces.com/api/v3, provider volcengine-ark; coding=doubao-seed-2-0-code-preview-260215(doubao-seed-coder非真模型)。ARK status字段缺失/null=活跃, Shutdown/Retiring=不可用。
§
拓扑(10/9最终态,决策A双活): gateway由webui gateway-runner监督(launchd ai.hermes.webui),exec ~/.local/bin/hermes→PM eddd树py3.14,10飞书bot稳定;launchd ai.hermes.gateway已bootout;git树留热备给webui agent-bridge(webui内部发现逻辑写死git树候选,plist env被覆盖,bridge翻不动PM,待webui原生支持agent-root后再退役)。hermes update前须确认两树同commit f42f579。备份~/.hermes/backups/switch-to-pm-20260930-205727/。
§
一人公司bot团队(11/2建): zongguan/neirong/chuangzuo/fenfa/chengzhang/biangu/kefu 7 profile,纯app侧;SOUL.md已写。旧九省六部9 profile已delete(墓碑),数据在~/.hermes/profiles/_liuju/。恢复:mv回_liuju/*。坑:命名profile不继承全局.env,AGNES_API_KEY须拷入;新bot首条消息可能Errno61(worker冷启动),重发即通。
§
MultiPost已弃用(11-11用户拍板): 清一AI账号发布一律ego直驱(见three-platform-publish skill), MultiPost扩展ego lite执行引擎不工作不再用