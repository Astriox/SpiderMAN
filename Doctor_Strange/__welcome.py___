import os
from pyrogram import Client, filters
from pyrogram.types import Message, User
from info import WELCOME, GOOD_BYE


@Client.on_message(filters.new_chat_members)
async def welcome(bot,message):
	chatid= message.chat.id
	await bot.send_message(WELCOME.format(user = message.from_user.mention, chat_name = message.chat.username), chat_id=chatid)                    
	
@Client.on_message(filters.left_chat_member)
async def goodbye(bot,message):
	chatid= message.chat.id
	await bot.send_message(GOOD_BYE.format(user = message.from_user.mention), chat_id=chatid)
	
