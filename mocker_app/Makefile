#/** @file
# * Copyright (c) 2019, Arm Limited or its affiliates. All rights reserved.
# * SPDX-License-Identifier : Apache-2.0
# *
# * Licensed under the Apache License, Version 2.0 (the "License");
# * you may not use this file except in compliance with the License.
# * You may obtain a copy of the License at
# *
# *  http://www.apache.org/licenses/LICENSE-2.0
# *
# * Unless required by applicable law or agreed to in writing, software
# * distributed under the License is distributed on an "AS IS" BASIS,
# * WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# * See the License for the specific language governing permissions and
# * limitations under the License.
#**/

C_FILES := $(wildcard *.c)
H_FILES := $(wildcard $(HEADER_DIR)/*.h)
OBJS := $(patsubst %.c,$(APP_OBJ_DIR)/%.o,$(C_FILES))

all: all_mocker_app

all_mocker_app: $(OBJS)
	@echo "### Finished building with makefile at `pwd` ###"

$(APP_OBJ_DIR)/%.o: %.c $(H_FILES)
	echo "$(CC) $(D_NAMES) $(CFLAGS) $(I_DIRS) -c $< -o $@"
	$(CC) $(D_NAMES) $(CFLAGS) $(I_DIRS) -g -c $< -o $@

clean: clean_mocker_app

clean_mocker_app:

.PHONY: clean
